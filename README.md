# kickstarter-analysis
# Kickstarting with Excel

## Overview of Project
This project seeks to provide valuable insights for Louise and her campaign funding endeavors. 

### Purpose
The purpose of this project is to utilize simple statistical analyses and render them in visually powerful ways to communicate kickstarter data to Louise and better inform her of her future campaigns, including where she may direct her focus to increase pledged funding and the success of future campaigns. 

## Analysis and Challenges
What follows is a detailed view into the process of organizing and displaying the campaign data in relevant and powerful ways to guide future decision-making for Louise.

### Analysis of Outcomes Based on Launch Date
To start, the first graphic displays theater outcomes based on launch date. After creating a 'resources' folder to hold the graphics, as well as a new sheet to store our data in a new table, I then added a 'years' column to the main spreadsheet, into which I used the =(year(cell)) formula to extra the year from the 'date created conversion' column. From there, I created a pivot table that allows the user to filter by year (filter category), subsequently displaying all months (rows) and their respective outcomes (columns). A possible challenge here can be accurately sorting these data into the correct fields, e.g. making sure outcomes is listed in both the 'columns' field as well as the 'values' (where it automatically becomes 'count of outcomes').

### Analysis of Outcomes Based on Goals
For this second analysis and its corresponding graphic, I also started by creating a new spreadsheet to hold our goal-specific data. This included eight columns: Goal, Number Successful, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Failed, and Percentage Canceled. (The last three are of vital importance and depend greatly on the first five columns.) The Goal column was the only non-formulaic column; it contained ranges for the funding goals of each campaign. The subsequent columns had formulas, for example, to calculate how many projects that had a goal of less than $1,000, we used:

=COUNTIFS(Kickstarter!F:F, "successful", Kickstarter!D:D, ">1000", Kickstarter!Q:Q, "plays")

This provided a count. We could do the same for 'failed' projects, changing "successful" to "failed" and finally adding the two with "canceled" to get a total projects count. 
From here, I applied Number Successful/Total Projects for Percentage successful. The same holds for 'failed' and 'canceled' columns. 
It's crucial to make sure that the 'total projects' column number is relative, so that it takes into account the respective ranges of funding goals. This could be a potential challenge for the data analyst. 

### Challenges and Difficulties Encountered
As noted above, it is very important to ensure that respective cell references are used when applying formulas to a specific range of goal funding. The opposite may hold true for other formulas that utilize a singular 'total count' cell across several rows and/or columns, though this wasn't the case in this analysis. The greatest challenge I saw was in selecting the correct data elements to display in my graphics. For the second graphic showing outcomes based on goals, we only needed to display the percentages, since the number of failed/successful/canceled projects alone lacked context to tell the whole story. This also applied to launch dates, where it was wise to remove 'live' projects that only encompassed one or two months at the beginning of the year. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
From this graphic, it is clear that theater operations launched in the early summer significantly more successful than those launched, for example, late into the year. October is an interesting month, since failures spiked while NO campaigns were canceled -- a sort of live by the sword, die by the sword situation. Finally, successful and failed campaigns almost mirror one another. This could suggest that, outside of canceled events, the more campaigns there are, the more there are both successes and failures; so depending on the number of campaigns, we can expect a respective increase or decrease in both categories. 

- What can you conclude about the Outcomes based on Goals?
The outcomes based on goals graph, since its data is more robust and more solidly incorporates the basic principles of statistical analysis. Noticeably -- and this was also mentioned throughout the course of the modules -- it would appear that "failed Kickstarter campaigns have much higher fundraising goals than successful Kickstarter campaigns.” We can see this clearly as the percentage failed skyrockets to 100% around and after the $45,000 goal range (with successful campaigns inversely at 0%). The opposite holds true for campaigns that requested less than $1,000 in funding, where the rate of success was almost 80%. It's also note-worthy to mention that 'canceled' campaigns were non-existant. What does this mean? Well, it's again a live by the sword, die by the sword approach: You're either likely to succeed or fail, with little room for middle ground. This could actually increase the amount campaigns initiated, in a sense making success more likely than the other two alternatives.

- What are some limitations of this dataset?
Limitations abound; but noticeably via country (most of it is in USA and Britain). Also, the  data only stretches from mid 2009 to 2017, so we are basing our analysis on an 8-year stretch, which may vary greatly when applied to the markets of a decade before or after. 

- What are some other possible tables and/or graphs that we could create?
It would be interesting to see tables comparing the different countries, particularly USA vs. Great Britain, where most of the data seems to stem from. On the other hand, it may be informative to see all other countries isolated from these two. Finally, I would suggest comparing funding goals across countries to see if successes and failures varied in the same fashion. 
