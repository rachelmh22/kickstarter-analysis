# Kickstarting with Excel

## Overview of Project

Since we have analyzed data for Louise to help her understand some of the factors involved in kickstarting a successful fundraising campaign, she would like to analyze the data again. This analysis shows compares different campaigns based on their launch dates and funding goals. 

### Purpose

The purpose of this project is to analyze and visualize data with Excel. We want to format the data to see how launch dates and funding goals affected different fundraising campaigns. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

In order to analyze the number of successful, canceled, and failed theatre productions based on the launch date, we need to use the year() function to extract the year from the column that holds that date of when the show was launched. This is because that column displays the year, month and date, but we are looking only for the year since we want to use that as a filter. We also want to filter to theatre, which means we also need to filter with the parent category that is already in its own column. We can create a pivot table on Excel since we have all the data needed. We put all the data into the correct places in the pivot table and then create a line chart from the table to illustrate the relationship between theatre outcomes and launch dates. From the pivot table, the month of May has the most number of successful shows, which can been seen in the chart as well. Whereas, October has the highest number of failed theatre productions but there are no canceled productions as well. 

### Analysis of Outcomes Based on Goals
The second analysis was performed to visualize the outcomes of plays based on their funding goal. This analysis is looking at more specific theatre productions- plays. Therefore, we need to filter the subcategory of the data in Excel to “plays”. Then we create a new sheet in excel that will count the number of successful, failed, and canceled plays based on their funding goals. For this analysis, we use the countif() function to fill the data in the new sheet. From this, we convert the numbers into percentages and create a line chart. From the line chart, we see that there are no canceled plays, regardless of the the funding goal. Additionally, the lines for the percentage of failed plays and successful plays move in opposite directions and there is an instance in the data where a funding goal had a 50/50 chance to produce a successful or failed play. 

### Challenges and Difficulties Encountered
The first challenge of this analysis was creating the correct pivot table. The issue was getting the table to display the months because the when the “date create conversion” field was placed in axis, the chart was showing years in the axis and I had to remove the “years” and “quarters” fields and leave just the “date created conversion” field in order to just get the months. 

The second challenge of this project was gathering the data for the outcomes of plays based on their funding goal analysis. The countif() function was needed in order to gather the data. The issue with using the function was inputing the correct information. The first row of data was simple to collect because the goal was less than $1000 so only one limit was needed in the function to count the number of outcomes based on that goal, as shown. 

=COUNTIFS(Kickstarter!F:F, "successful",Kickstarter!$D:$D, "<1000",Kickstarter!R:R, "plays")

However, when the next goal was between two goal amounts, $1000 to $5000, I only used one limit. I would set the countif() function to count the outcomes if they were less than $5000 only. I learned that two limits needed to be placed in the function to properly count the outcomes between $1000 and $5000, as shown. 

=COUNTIFS(Kickstarter!F:F, "successful",Kickstarter!$D:$D, ">=1000",Kickstarter!$D:$D, "<=4999", Kickstarter!R:R, "plays")

## Results

### What are two conclusions you can draw about the Outcomes based on Launch Date?

In regards to the Outcomes based on Launch Date analysis, it can be concluded that the best time to launch a theatre production is in May and the other summer months. These months, and especially May, have the highest number of successful outcomes. However, May also has the highest numbers of failed theatre productions but since May displayed the highest number of productions launched, the failed plays are relatively small in relation to the number of plays launched. Unlike in October, where there is the second highest number of failed theatre productions but the number of launched theatre productions is lower so the failed amount is more significant in October. 

The second conclusion that can be drawn is to avoid launching a show in December. The results shows that December is the month that has the least number of launched theatre productions. In addition to productions being launched less in December, these productions have similar chances of being failed or successful since the number of failed and successful productions in December is about the same. 

Based on the data, it is more beneficial to launch a theatre production in May and most disadvantageous to launch in December. 

### What can you conclude about the Outcomes based on Goals?

Based on the Outcomes based on Launch Date analysis, it can be concluded that the most successful plays are

### What are some limitations of this dataset?

The limitations of this dataset is that the data is filtered to one category. A single category does not reflect the results for all categories of fundraising campaigns. While it is beneficial to launch a theatre production in May, this may not be true for fundraising campaigns based on food or music. It is possible more people are interested in going to shows in the summer months but it may not be true for other categories like journalism. An author launching a children’s book would not launch in May since this data is only for their productions. 

The same is true for the data in the Outcomes based on Goal analysis. The data is only representative of plays. While the funding goal of less than $1000 or around $40,000 is shown to be most successful to plays, that could be different for other categories, like television shows or electronic music. This is data is limited in use and cannot be applied to all funding raising campaigns. 

### What are some other possible tables and/or graphs that we could create?

We could create a stacked bar graph for the the outcomes on goal analysis and show each bar as an outcome. A pie chart could also be a great visualization for the data since the data is displayed in percentages, so multiple pie charts could be created for each funding goal amount.
