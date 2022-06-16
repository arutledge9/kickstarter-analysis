# Kickstarting with Excel

## Overview and Purpose of Project

I am conducting analyses of theater and play Kickstarter projects for Louise after the success of the Kickstarter for her play, Fever. The purpose of these analyses are to determine how Kickstarter theater projects’ launch dates and how Kickstarter play projects’ goal amounts affect their outcomes. It’s the hope that the results of these analyses will further inform Louise as she continues to successfully fund her work.


### Analysis and Challenges – Theatre Launch Dates


In analyzing theatre launch dates, I filtered our Kickstarter data by the Theater Parent Category. ![](/Resources/filter%20for%20theater.png) I then created a column of launch date years using the `=year()` formula on the Date Created Conversion column, and then created a Pivot Table in sheet *Theater Outcomes by Launch Date* to further analyze the Kickstarter outcomes. I made sure to include filters in the Table for my Parent Category and my new Years column, while creating a Table column for outcomes and a Table row for months of the year. Finally, I outputted the outcomes field again as values and sorted my data fields within the Table before creating a Pivot Chart to easily digest the data. I chose a line chart to represent the change in outcomes over time. ![](/Resources/theater%20pt%2C%20pc.png)

I found it challenging to find where to sort my outcomes on the Theater Outcomes by Launch Date pivot table. I originally looked to the PivotTable Fields sections in Legend(Series) and Values where I had dragged the outcomes field until I realized I should be looking in the filtered Column Labels in the Pivot Table itself. Once I was in the Table and looking at the Column sorting options, they made perfect sense. I looked to the Table’s rows and found a sort-by-age option for the Months as well, which reinforced what I was seeing.

I also wasn’t able to figure out how to remove the fields placed into the Pivot Chart from the Pivot Table, such as *Years,* *Count of outcomes,* and *Date Created Conversion.* I noticed these fields weren’t present in the Textbook example and thought that example looked much cleaner and more digestible for an audience. 




### Analysis and Challenges – Play Goals

I first filtered my Kickstarter data on the Subcategory Plays. ![](/Resources/filter%20for%20plays.png) I then created a new sheet called Outcomes Based on Goals, created a row for Goal ranges, and then set out to create formulas using the CountIfs() formula to tally up specific Kickstarter campaign outcomes for plays for each Goal range. Following this, I totaled the projects from the number of outcomes per goal range, calculated percentages for each outcome from the whole per goal range, and then plotted the outcome percentages per goal range on a line chart for easy viewing. 

It was so challenging figuring out the CountIfs() formulas! Not because of the syntax, but by not making the connection that my initial formulas of ` =COUNTIFS(Kickstarter!D:D,"<1000")` and ` =COUNTIFS(Kickstarter!D:D,">=1000", Kickstarter!D:D, "<=4999")` in my new sheet weren’t going to equal the numbers in my Kickstarter sheet when I manually proofed the counts, because my Kickstarter sheet was *filtered on plays* and I hadn’t added that filter to the CountIfs() formulas yet! Not realizing this discrepancy ate up an embarrassing amount of my time and let forth many new combinations of curse words I didn’t realize I was capable of uttering. But I do love making mistakes(after the fact), as they’re a great teacher – these mistakes reinforced the fact that filters on a spreadsheet in Excel do not transfer over when you create a Pivot Table (as in our first analysis, where we needed to filter on theater in the Pivot Table regardless of filter settings in the Kickstarter sheet) and here in this example when you instruct the program to run a formula on an entire column (and even if you’re in the same sheet, which I find odd). I also find it quite funny now to realize that I never needed to filter any Categories on the "Kickstarter" sheet itself.




### Analyses Results and Discussion

I was able to conclude that the highest chances for successful theater Kickstarter campaigns occur when they are launched in May, June, and July, respectively. Interestingly, the most failed Kickstarter campaigns also occur in May, but that’s more of a function of May being the month with the most campaigns launched. The worst month to launch a theater Kickstarter is in December, the only month where the successful outcomes barely squeak above the failed outcomes.

Play Kickstarter campaigns are much more successful the lower their goal amounts are, specifically goals $14,999 and under, and within this amount, goals less than $1,000 and goals between $1,000 and $4,999 having the best chances for success respectively. I would, however, caution Louise on setting a goal between $10,000 and $14,999, as the success rate in this goal range is only 54.17%, and we also have a rather limited number of Kickstarters to analyze in this range (72), versus nearly 900 in the previous three brackets. While some goal ranges above $20,000 appear successful, the very limited number of campaigns with these goal amounts suggest extreme caution since we have very limited data.     

A concern for Louise with our data in general is that the data we’re looking at is all becoming aged, with the bulk of the theater Kickstarter campaigns falling between 2014, 2015, and 2016. We only have limited data for 2017 (January and February) and then our data set ceases. I would like to obtain a completed set of 2017 data as well as information from 2018-present before presenting findings to Louise. In addition, the fact that we only have three years forming the bulk of our data is not ideal. So these two limitations – the age of our data and the somewhat narrow spread of our data over time – give me pause in what I feel I could confidently tell Louise about theater and play Kickstarter performances to inform her decision making in mid-2022 and beyond.

Further analyses benefitting Louise would be ones delving deeper into the most successful data points we’ve uncovered. We now know that the most successful theater Kickstarters are launched during May, June, and July, and that the most successful play Kickstarters have goal amounts below $5,000. A chart examining the intersection of these data points would be fascinating – are Kickstarters with goals below $1,000 launched during May the most successful by and large? What if Louise says, “Well, my play needs at least $3,500 to get off the ground”? Then we can chart how well plays at that amount and above (say, up to $4,999) perform during the spring and summer time period to determine the optimal launch date and goal amount for Louise based on past Kickstarter performances. 


