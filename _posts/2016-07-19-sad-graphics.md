---
layout: post

title: Data visualizations good and bad
description: Even major media outlets produce confusing graphics

author: Steven Porter
email: stevenporter2016@u.northwestern.edu
twitter: reporterporter
---

## Data visualization is storytelling, whether intentional or otherwise

Scrolling through my Twitter feed yesterday, I came to a post by Bloomberg and halted. The tweet contained a chart that showed stock prices plummeting over a hair-raising cliff, with the question, "Is 'Star Wars' played out for Hasbro?"

I lingered and noted the ominous next line: "Putting Away the Toys." Inhaling just enough air to blurt, "Think of the children!" I halted again, recalling recent data visualization lessons still fresh in mind from the digital frameworks course.

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Is &quot;Star Wars&quot; played out for Hasbro? <a href="https://t.co/M43iNFiG2K">https://t.co/M43iNFiG2K</a> <a href="https://t.co/yNA1lhuY7E">pic.twitter.com/yNA1lhuY7E</a></p>&mdash; Bloomberg (@business) <a href="https://twitter.com/business/status/755125027184504837">July 18, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

It's not until I read the thirdmost-prominent line of text that the chart's meaning came into focus. Hasbro shares fell as much as 7 percent in intraday trading Monday. Oh, that's bad. But it's not the cataclysmic ralph-inducing rollercoaster ride I'd been expecting.

Instead of beginning at $0 per share, the y-axis begins at $79 and ends at $86, dramatically exaggerating the slope of the downward trend in Hasbro's valuation. It's understandable that Bloomberg would find this chart more compelling than one with a y-axis from $0 to $86, but the more compelling version isn't supported by the story. As a news consumer, this feels like clickbait. (Perhaps the headline should read, "You Won't Believe How Far Hasbro $$tock Plummeted Today!")

Perhaps the sneakier issue with this graphic is in its x-axis. Prices are holding steady between $85 and $86 per share until suddenly the floor falls out from underneath them. What the chart fails to mention is that there was a weekend between the holding-steady and the plummeting. Share prices were $85-86 on Friday, then they dropped dramatically Monday morning after a two-day trading hiatus. If the chart were showing price trends over recent weeks, months or longer, then marking the weekends and holidays would be entirely unnecessary; in this case, however, when we're looking at just two days of trading, it seems like that gap is key information we're missing.

Clearly, Bloomberg's target audience is savvy enough to read this chart properly the first time. But there are lessons here for all visual storytellers, especially those of us targeting a more general audience. Although zooming in on the y-axis by limiting its range can make the newsworthy movement more obvious, it can also prove misleading by telling an exaggerated tale. It's important to remember that charts like this one are meant to convey meaning found in the relationship between two data points — in this case time and stock price — so we should ask ourselves whether omitting seemingly irrelevant segments of the x-axis might impede a consumer's understanding of that relationship.

## Enough with the bad stuff; show me the good

To counterbalance all the negativity, I wanted to share with you a data visualization that, despite its complexity is entirely comprehensible and compelling. But before I show it to you, I wanted to highlight a particular sentence to reiterate my point that data storytelling is still storytelling.

In the lede to his <a href="http://www.nytimes.com/2016/07/20/upshot/hillary-clinton-has-a-76-percent-chance-to-win-the-presidency.html?action=click&contentCollection=upshot&region=rank&module=package&version=highlights&contentPlacement=2&pgtype=sectionfront">New York Times story</a> today about the latest polling numbers, Josh Katz made things plain and simple:

<blockquote>For now, at least, Hillary Clinton has a 76 percent chance of defeating Donald Trump to become president of the United States.</blockquote>

That seems simple enough, right? Perhaps. But Katz made the wise move to take things a step further with his next sentence:

<blockquote>A victory by Mr. Trump remains quite possible: Mrs. Clinton’s chance of losing is about the same probability that an N.B.A. player will miss a free throw.</blockquote>

Even though I don't care about basketball in the least, I find that illustration entirely relatable. I understand that pro players tend to make their free throws, but it's not a surefire thing. The word picture works.

Now on to the visualization. It's large and interactive, so you'll have to go <a href="http://www.nytimes.com/interactive/2016/upshot/presidential-polls-forecast.html?action=click&contentCollection=upshot&region=rank&module=package&version=highlights&contentPlacement=3&pgtype=sectionfront">here, "How Other Forecasts Compare,"</a> to check it out.

What I love about this visualization is how, instead of simply reporting its own data, the New York Times opted to compare and contrast predictions by seven different pollsters to parse out Katz's lede. The graphic effectively color-codes each pollster's prediction state by state, deftly employing variation in color density to convey variation in percentage of voters expected to vote one party or the other. The pale yellow used for states that aren't clearly going to vote Republican or Democrat works because it appropriately highlights them as the places where we can expect concentrated campaign activity between now and November.

The graphic tells the same story as Katz's lede because it places solid Blue states on top, followed by swing states, then Red ones at the bottom. It would be no less accurate to reverse this order; however, that would clash with the focus and framing of the story as written. For a story about "The X states Donald Trump needs to win to become our 45th president," or something like that, I would expect the New York Times to give us a graphic with the Red states on top.

