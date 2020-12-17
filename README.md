# Kickstarting with Excel

## Overview of Project
### Purpose
Our client, Louise, wants to raise funds for a theater production using Kickstarter, and so we obtained Kickstarter data consisting of project campaigns for the arts, technology, and media in order to evaluate the data for takeaways relating to relationships between the outcome of a Kickstarter for theaters and two variables: 1)when the campaign took place and 2) what the campaign's goal was. Ultimately, we want to help Louise have the best chance at a successful Kickstarter campaign, so we're using the data available to us do make our best recommendations.


## Analysis and Challenges
We first wanted to assess outcomes by things like seasonal trends over the course of a 12-month timeframe, for example, to see if there are months that have a particularly high or low chance toward success. Next, we wanted to see how the campaign outcomes compared and contrasted by fundraising goal, to learn if there is a formula for a successful financial goal. Below is each step in more detail.


### Analysis of Outcomes Based on Launch Date
For the assessment based on launch date, we had to first start by converting the launch date from a "short date" format to the year it was launched, using the YEAR function. Then, we created a pivot table broken out by months on the x-axis and outcomes ("successful", "failed" and "canceled") on the y-axis , with the populated data being the number of outcomes for each category. The table is then filtered by "parent category" and "years". 

For a visual side-by-side comparison of our filter to only include theater-based campaigns, we created a line chart. Below is that chart, entitled "Theater Outcomes by Launch Date" with the results.

![Alt text](https://github.com/andeevosters/kickstarter-analysis/"Theater_Outcomes_vs_Launch.png")

### Analysis of Outcomes Based on Goals
To do a more refined assessment of the outcome by fundraising goal, we only looked at play kickstarters. We then categorized the data into 12 $goal groups in $5,000 increments, starting at "less than $1,000" and up to "$50,000 and greater". We counted the number of outcomes in each of the outcome categories using the COUNTIFS function, added all the possible outcomes together per goal range using the SUM function, then determined the percentage of each outcome type by dividing the outcome type by the total projects and formatting the cell as a percentage.

The "Percentages of Outcomes Based on Goals" chart can be found below.

Outcomes_vs_Goals.png

### Challenges and Difficulties Encountered
Overall, there weren't many difficulties in doing this analysis. If you need some refreshing of Excel, however, here are a few things to consider.
1. Because we wanted to analyze our first set of data by years, it took a bit to figure out how to break the year into months. It's worth Googling how to filter a year into months and quarters inside a pivot table.

2. There is a small set of data that doesn't fall into the three outcomes defined by the assignment (successful, failed and canceled). This set is "live". A decision will need to be made on whether to include that data in the sample, if it means your results look different than what you're being asked to report. In our case, we weren't asked to report "live" outcomes. I chose to include them in my sample, but others may not have.

## Results
### Results of Outcomes Based on Launch Date
1. There were not many campaigns prior to 2014 (81 Kickstarters). The majority of campaigns ran from 2014 to 2016 (1,312).
2. Rarely were theater-based fundraising campaigns canceled, and if they were, no month stood out as a high- or low- cancelation month. This might imply tenacity on behalf of the campaign managers.
3. May was by far the most successful month for meeting campaign goals (111), whereas the winter months generally fared the lowest (37 in December). (It is worth noting that there is a peculiar, short spike in February in overall Kickstarters, but particular successful ones.)

### Results of Outcomes Based on Goals
Anything under $5,000 has roughly a 75% success rate, and has a steep decline in success as the goal goes higher (except for a surprisingly successful outcome in the $35,000 to $45,000 category for 6 Kickstarters, but we know that range isn't relevant to Louise's goals).

Also based on the chart we analyzed, I would recommend that Louise launches her Kickstarter in May for a June or July finish. May reports the highest number of successful Kickstarters, but it's important to note it also reports the highest number of failed Kickstarters. However, the number of successful campaigns more than double the failed ones (111 vs. 52). 

### Some limitations of the dataset
While these two datasets were helpful to see the landscape of Louise's fundraising hopes, they do not tell the whole story. For example,
- Based on the sheer drop in success after a campaign goal exceeds $5,000, the chart we created doesn't give us the desired detail of success within the $0-5,000 range.
- It's not as much about the sheer number of campaigns that determine a recommended launch date (ex. May with 111 Kickstarters vs. 37 in December), as much as it is the likelihood of success in a given month. And that is easier to determine using percentages (67% in May vs. 49% in December).
- It's possible that the length of the Kickstarter will play a role in a campaign's success.

### Other potential datasets and visuals to help deliver a solid recommendation
To give our best, most-assured recommendation, I'd suggest also analyzing the following, at a minimum:
- Look at the launch date data as a percentage, not just numbers.
- Splice out the $0-5,000 data into smaller subsets, perhaps in $1,000 increments.
- Look at data subsets by outcomes(for plays only) categorized by the following:
   - Length of a Kickstarter (#weeks from launch to end)
   – Number of backers (start by 100, then splice as needed from there). This in particular will help to determine your necessary marketing efforts for your fundraiser.

### If I had to give a recommendation based on this dataset:
If I were to give Louise my recommendation on the best fundraising goal based on the data analyzed, it would be not to surpass $4,999, and to run the campaign in May with a June or July end date. However, there are opportunities to give a considerably more educated recommendation with further analysis (using the recommendations above).
