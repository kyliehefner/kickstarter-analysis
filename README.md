# Kickstarting with Excel

## Overview of Project

### Purpose
The client has recently launched a Kickstarter for a play and is interested in the outcomes of other Kickstarter campaigns based on their launch dates and funding goals. The project's goal was to uncover insights and trends among other theater and play Kickstarters and visualize the outcomes for the client.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
#### How the Analysis was Performed
To perform this analysis, I created a pivot table listing the number of campaigns sorted by their outcome (successful, failed, canceled) and their launch month. Then I filtered the data only to include theater campaigns since that is the category of our client's campaign and created a line chart to compare the successful and failed campaigns over the year.
#### Results of Analysis
An analysis of the outcomes based on launch date reveals that campaigns launched in May and June are significantly more likely to be successful than campaigns launched in other months. Filtering by only theatre campaigns reveals that this trend is even stronger in theatre, with May, June, and July having significantly higher rates of success.

![OutcomesBasedOnLaunchDate](https://github.com/kyliehefner/kickstarter-analysis/blob/0dc6978f96b98b46e908b40e8e84badc72c30345/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
#### How the Analysis was Performed
To perform this analysis, I used Excel's COUNTIFS() function shown below to calculate the number of Kickstarters in the play subcategory based on their outcome among 12 different goal ranges. Then I calculated the percentage of Kickstarters with each outcome in the 12 goal ranges. A line chart of this data shows the percentage of each outcome based on the initial goal amounts for the campaigns.
```
=COUNTIFS(Kickstarter!$F:$F, "successful", Kickstarter!$D:$D, "<1000", Kickstarter!$O:$O, "plays")
```
#### Results of Analysis
Based on this line chart, we can see that plays with a goal of less than $15,000 or between $35,000 and $44,999 had a higher proportion of success, while plays with a goal of between $19,999 and $34,999 or over $50,000 had a higher proportion of failure. These results have a smaller margin of error for plays with lower goals since our data is skewed heavily toward smaller goal amounts. Since there are only a handful of plays with large goals in our data set, the sample proportion of successful plays for higher goals is less reliable.

![OutcomesBasedOnGoals](https://github.com/kyliehefner/kickstarter-analysis/blob/0dc6978f96b98b46e908b40e8e84badc72c30345/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
#### Sample Size
The main issue faced in this analysis is our sample data sample size. Our data set includes 1,369 entries in the theater category and 1,047 entries in the plays subcategory. While this is a large sample size, we also must pay attention to our marginal distribution sample sizes. In our analysis based on launch date, we had a small sample of canceled theater Kickstarters, so the data for that category has a large margin of error. In our goal-based analysis, we had a small sample of Kickstarters with high goals, so that data is also more likely to be unreliable. Therefore, the results for campaigns with high goals should not be used to predict the success of similar future campaigns accurately. However, since we have a large sample size of small goal campaigns, the results from that data are more reliable.
#### COUNTIFS() Calculations for Goal-Based Analysis
A potential challenge with this analysis could be creating the COUNTIFS() calculations. Close attention to detail needs to be taken that the goal categories do not overlap and that the data on the campaigns' goals are used, not the funded amounts. It is also essential to be aware that the goal categories we picked are not all the same size, with the first 2 categories being 1/5th and 4/5th the size of the higher categories.

## Results

- My analysis of the outcomes based on launch date reveals that theater campaigns launched in the summer months (May, June, July) are significantly more likely to be successful than campaigns launched in other months of the year. We can also conclude that campaigns launched at the end of the year (November, December) are less likely to be successful than campaigns launched in other months. We don't have enough data on canceled campaigns to make any conclusions about them based on launch date

- The analysis and line chart of outcomes based on goals reveals that plays with a goal of less than $15,000 or between $35,000 and $44,999 had a higher proportion of success, while plays with a goal of between $19,999 and $34,999 or over $50,000 had a higher proportion of failure. The results of our analysis are most accurate on the lower range of goals due to sampling size.

- The sample size is one limitation of this dataset because we have small sample sizes for our marginal distributions of canceled theater campaigns and plays with large goal amounts. Therefore our results are less reliable for these populations. Another potential limitation is the lack of nuance in the success category of our analysis. For example, a campaign could be funded 98% and labeled as failed, while campaigns labeled successful can range from 100% to 6,500% funded. We could use different visualizations or more outcome categories to differentiate further in the future.

- We could create another pivot table for the outcomes based on the time between the launch date and end date to see if the length of the campaign affects the success rate. Using that table, we would create a line chart of the number of campaigns vs. the campaign length (divided into sections) with lines for successful, failed, and canceled campaigns. We could also edit our existing graphs to focus on theater campaigns similar to our client's, such as filtering the outcomes based on the launch date line chart to include only recent years or creating smaller partitions of goal amounts in the outcomes based on the goal line chart.
