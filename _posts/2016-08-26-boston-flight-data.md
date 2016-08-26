---
layout: post

title: Linear regression with Boston airport data.
description: Learning data journalism tools with real-world numbers.

author: Steven Porter
email: stevenporter2016@u.northwestern.edu
twitter: reporterporter
---

## Making simple but sound predictions with data

To practice working with data, I downloaded <a href="https://data.cityofboston.gov/Finance/Economic-Indicators/snhc-w7k7">a simple spreadsheet</a> with monthly economic indicators for Boston in 2013 and 2014. In addition to commonly cited unemployment rates and new home construction permit figures, the data include traffic information for Logan International Airport.

Each month, the city reports how many flights and travelers fly through the airport, holding up the numbers as an indicator of economic activity. It would make sense if the number of travelers and the number of flights were positively correlated, but I wanted to know from a data perspective the extent of their correlation and what that might mean for the city.

So I imported the spreadsheet <a href="
https://docs.google.com/a/u.northwestern.edu/spreadsheets/d/100nBryY-g4BN3lvTQeLi_dfZMGURlHVbVimNz7H0WZg/edit?usp=sharing
">into Google Sheets</a> and ran a scatter plot then a linear regression comparing my two columns:

<iframe src="https://docs.google.com/spreadsheets/d/100nBryY-g4BN3lvTQeLi_dfZMGURlHVbVimNz7H0WZg/pubchart?oid=195274335&amp;format=interactive" width="650" height="400"></iframe>

As expected, the regression line confirmed the correlation: months with more flights saw more passengers, too. (This, of course, doesn't demonstrate which variable, if either, caused the other.)

Beyond merely showing the correlation, I had Google tell me how closely the regression line matches the scatter plot, using the R-squared feature. At 0.86, the match is relatively strong.

By hovering over the regression line, I see its formula, which tells me the y-intercept: 629. That means the regression line thinks there would still be 629 flights each month in and out of Logan International Airport in a month when there are zero passengers. Clearly, this calculus isn't going to prove terribly useful to policymakers discussing low numbers of flights and passengers. It could, however, prove useful when they're talking about growth potential, especially since the city tracks these numbers as economic indicators.

Let's say the mayor began touting a plan to boost economic activity in Boston by doubling the number of passengers traveling through the airport each month. Instead of 2.5 million average monthly passengers, the mayor wants to see 5 million or more. Based on existing data, we can now predict the approximate number of flights needed to achieve the mayor's objective: 5,724. (That's a 77-percent increase over the monthly average of 3,235 flights.)

With this calculation in hand, a reporter could then ask a dozen air traffic controllers whether the airport could handle that many flights. If not, then the mayor has more explaining to do.

