# An Analysis of Kickstarter Campaigns

## Overview of Project
The client is interested in starting a Kickstarter campaign to fund a play. This project contains analysis of crowdfunding Kickstarter data. The analysis focuses on crowdfunded plays in the United States.

### Purpose
The goal of the project was to uncover insights and trends among successful and unsuccessful campaigns so that the client will make educated decisions about how to run her campaign.

## Analysis of Outcomes Based on Categories and Subcategories
First we found that of all the parent categories on Kickstarter, theatre campaigns were the most popular, but not the most successful. Yet of all theatre campaigns from out data set, over 500 out of the 900 campaigns were successful.
![ParentCategoryOutcomes](https://user-images.githubusercontent.com/102445183/162046499-90ffab47-d9d5-468f-9694-371fe588d1b5.png)

Digging deeper into the subcategories, we found that plays account for the majority of the theatre campaigns, and are again over 50% successful. The high volume of sample data categorized as plays is a good sign that our data analysis will be accurate to the population.
![SubcategoryOutcomes](https://user-images.githubusercontent.com/102445183/162046915-8a9991d8-f72d-4cd6-9836-e3f272c2e5d8.png)

### Analysis of Outcomes Based on Launch Date
An analysis of the outcomes based on launch date reveals that campaigns launched in May and June and significantly more likely to be successful compared to campaigns launched in other months of the year. Filtering by only theatre campgains reveals that this trend is even stronger in theatre, with May, June, and July all have significantly higher rates of success.
![LaunchDateOutcomes](https://user-images.githubusercontent.com/102445183/162047631-fe0e60a1-c689-4e32-9a4a-2a1734089b6d.png)

### Analysis of Outcomes Based on Goals
Looking at descriptive statistics of US play Kickstarters we see that the mean and median goal of failed Kickstarters is about twice the mean and median goal of successful Kickstarters. However, the mean and median pledged amount for failed Kickstarts is about 1/10th the amount of successful Kickstarters, revealing that the higher average goal is likely not the reason for the failure of most Kickstarters. We also found that the mean goal and mean pledged were both around the 3rd quartile of the distributions, and that the distributions are heavily skewed right, with a high concentration of Kickstarters below the mean. Based on this analysis it is clear that there are outliers on the high end of Kickstarter goals and pledged amounts that are skewing the data.
![OutcomesBasedOnGoals](https://user-images.githubusercontent.com/102445183/162052962-d0ee06c5-d5cf-4859-a24d-99cd625e1a06.png)
