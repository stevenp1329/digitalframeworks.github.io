---
layout: post

title: Pulling and parsing daily jail booking data
description: Feeling a bit nostalgic about my days as a local crime reporter

author: Steven Porter
email: stevenporter2016@u.northwestern.edu
twitter: reporterporter
---

Before returning to school, I was a crime and justice reporter in Lafayette, Indiana, where I reviewed the latest booking records at the Tippecanoe County Jail each morning (and many afternoons).

The ritual unveiled more than a few daily news stories, including the wholly unexpected <a href="http://www.jconline.com/story/news/crime/2015/07/11/church-music-pastor-arrested-voyeurism/30013533/">Saturday-morning story about a local music pastor's arrest</a> for alleged voyeurism with a camera.

Jail records are updated online every 30 minutes in <a href="http://www2.tippecanoe.in.gov/inmates/inmates.aspx">an easily accessible, sortable table</a>. So it wasn't too onerous a chore to check in regularly, but it's easy to get distracted and forget. And the number of inmates was big enough that calculating any bulk information about them manually wouldn't be worth the hassle.

Thanks, however, to import.io (a data extraction tool I'm learning to use through the Digital Frameworks course I'm taking) I'm able to automatically pull the booking data every morning at 5 a.m. into <a href="https://docs.google.com/a/u.northwestern.edu/spreadsheets/d/1_im6MN9_WptdgaxaER_47mtD9d1lL-I20hd4OMBBWBM/edit?usp=sharing">a Google spreadsheet online</a>.

If I were to learn <a href="http://www.computerworld.com/article/2469616/business-intelligence/business-intelligence-79661-how-to-create-an-automatically-updating-spreadsheet.html#slide9">some additional coding</a>, I could teach that spreadsheet to automatically store historical data each morning as well. For the time being, though, I'm going to focus on a couple of one-day bulk-data questions I wasn't able to easily answer during my stint as a crime reporter.

# How long have these people been in jail?

There are all sorts of deadlines police and prosecutors must meet to keep a suspect in custody, so it's always helpful to know where each defendant stands in that process. Although it's relatively easy to pluck any single booking report from the list and mentally calculate how long he or she has been in jail, I wanted to know how many days have elapsed since each and every inmate was booked.

So I added a new column and used the following formula in every row with data: =DATEDIF(H2,TODAY(),"D"), where H2 refers to the cell in each row in which the booking date and time are recorded. That formula left me with a number from 0 to 791 days. (I copied the entire import.io data set for Aug. 15 and pasted it, values only, <a href="https://docs.google.com/a/u.northwestern.edu/spreadsheets/d/1_im6MN9_WptdgaxaER_47mtD9d1lL-I20hd4OMBBWBM/edit?usp=sharing">in a new tab</a>.)

This new, static spreadsheet tab allows me to sort the booking records by length of incarceration (which renders the same order, of course, as sorting by booking date). But it also allows me to add a column to reclassify/redescribe that length of time. I want to know who's been in jail less than a week, more than a week but less than a month, more than a month but less than three months, and more than three months.

So I added a new column and used the following formula in every row with data, with J2 referring to the cell in each row in which I placed the DATEDIF formula above: =IF(J2<8,"a 0-7 days",(IF(J2<31,"b 8-30 days",(IF(J2<91,"c 31-90 days","d 90+ days"))))).

This enabled me to create a pivot table, which I used to determine that, on Aug. 15, out of the 428 people in jail, 66 of them (15 percent) had been there a week or less. Another 107 (25 percent) had been there more than a week but less than a month.

More than a month but less than three months? 129 or 30 percent. More than three months? 126 or 29 percent.

That pivot table enabled me to visualize the jail population's length of incarceration with a histogram:

<iframe src="https://docs.google.com/spreadsheets/d/1_im6MN9_WptdgaxaER_47mtD9d1lL-I20hd4OMBBWBM/pubhtml?gid=1401009722&amp;single=true&amp;widget=true&amp;headers=false" width="650" height="400"></iframe>


