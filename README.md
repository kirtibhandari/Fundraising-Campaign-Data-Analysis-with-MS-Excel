# **Kickstarting with Excel**

## Overview of Project
We have a dataset which contains information about different fundraisng campaigns in various countries of the world, in different start and end dates, for a number of categories, providing valuable information about the campaign's financial goals, what amount was pledged against each such campaign along with their outcomes when they finished.

### Purpose
On the basis of the available dataset, we are required to find out which campaigns achieved their fundraising goals successfully , which could not and which were cancelled. Also, how the outcomes were affected by amount of funds that were designated as goals as well as how the launch dates impacted those outcomes.

For current analysis, there are 2 visualizations. Firstly, a visualization to represent outcomes such as successful, failed and canceled, of 'Theater' Parent Category for all the years, on the basis of Launch month of the respective year.

Second visualization to depict relationship between goals of campaigns and what percentage of those campaigns were successful, failed and canceled depending upon amount of fund they wanted to be raised for them. 


## Analysis and Challenges
 Explain how you performed your analysis using images and links to code, as well as any challenges you encountered and how you overcame them. If you had no challenges, describe any possible challenges or difficulties that could be encountered.

Before we can perform our analysis, we need to check if we have the required information or required values in required format in available data set or do we have to convert any available information or create new columns, or do we need to apply filters to extract any specific values out of already available values in a column, to have required information for our analysis. This basically we can say, cleaning or organising data. So, required columns were created, pivot tables and charts were made.

### Analysis of Outcomes Based on Launch Date

To do analysis of outcomes based on Launch Date, a new coulmn 'Years' was created by extracting value of 'Year' from the available 'Date Created Conversion' column so that we can see how 'Theater' campaign performed over years. To do this, Excel YEAR(serial number) function was used.

![Years_Column](https://github.com/kirtibhandari/Module-1-Challenge/blob/main/Resources/Years_Column.png)

Next, a pivot table was created using 'Insert' tab --> 'Pivot table' -->'New WorkSheet'

![Pivot table- Launch Date](https://github.com/kirtibhandari/Module-1-Challenge/blob/main/Resources/Pivot_Table-Outcomes_Based_on_Launch_Date.png)

After placing relevant fields columns, rows and values, we have the following Pivot Table :

![Outcomes by Launch Date initial](https://github.com/kirtibhandari/Module-1-Challenge/blob/main/Resources/Outcomes_by_launch_date_inital.png)

Since we need analysis, on the basis of 'Theater' Parent Category and , over the period of months, Year wise, we need to group data , month wise, so that we can choose year from the filter, for data of years, we do grouping as below, by right click on first value, then 'Group' --> 'Months' :

![Grouping process](https://github.com/kirtibhandari/Module-1-Challenge/blob/main/Resources/Grouping.png)

Next, we obtain following result after grouping row labels on 'Month' basis, Filtering Parent Category on 'Theater' basis and sorting the columns so that 'successful' is shown first.

![After Grouping, Filtering & Sorting in Descending Order](https://github.com/kirtibhandari/Module-1-Challenge/blob/main/Resources/After_Grouping_and_Filtering.png)

Next, we want to create a visualization for simplifying and comprehensible for our client, we create a Pivot Chart (Line Graph), to depict realationship between outcomes & launch months, for 'Theater' Parent Category, over period of all Years down the line, using Pivot Chart option .

![Pivot Chart Option](https://github.com/kirtibhandari/Module-1-Challenge/blob/main/Resources/Pivot_Chart_Option.png)

As a result, we obtainf below line chart, presenting relationship betwee outcomes and luanch month, as required.

![Theater Category - Outcomes_vs_Launch](https://github.com/kirtibhandari/Module-1-Challenge/blob/main/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
To do analysis for campaigns' Outcomes how they faired when we see them against 'Goals', in terms of percentage of success, failures or cancellation varying depending upon the target fund they aimed at raising, we need to know how many were a success, failure or cancelled against Total campaigns.

For this, a new worksheet was created, counts of campaigns, counts of success, failures and cancellations were made and then their percentage was calculated,among different goal amount ranges, and sheet was named ' Outcomes based on Goals'.

![Dataset_Outcomes_Based_On_Goals](https://github.com/kirtibhandari/Module-1-Challenge/blob/main/Resources/Dataset_Outcomes_Based_on_Goals.png)

Then we created a Pivot Chart (Line Chart) to create a visulaization on the basis of this dataset, plotting goal amount ranges vs percentage of successful , failed or canceled projects. The resulting graph as below:

![Outcomes_vs_Goals](https://github.com/kirtibhandari/Module-1-Challenge/blob/main/Resources/Outcomes_vs_Goals.png)


### Challenges and Difficulties Encountered
#### Outcomes based on Launch Date
There were couple of requirements that were new though knew basic use of Excel.
1. Use of YEARS function - to extract year part from Date. Column value format for 'Date Created Conversion' was 'Short Date' previously when this column was created. To get the exact format as in the required screen shot with date format and time of that day, i had to first convert this 'Date Created Conversion' columns format Using 'Custom' option and then choosing appropriate format.

2. Second, grouping data just to be able to display Months, had to learn it from the video tutorial embedded in the challenge.

#### Outcomes based on Goals
Use of COUNTIFS function of excel was a bit tricky as it involved somewhat complex syntax. I was unable to initially acheive the required graph. Then I found out I missed out one symbol while using the formula. So, it helped me understand that proper focus is required while performing complex calculations, especially when you are learning some new functionality in order to acheive the required outcomes.


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

1. More success was achieved in months of 'May'or 'June' and least in months of 'Nov' and 'Dec'. Hence, we can indicate our client when they can think of launching a campaign would be better as compared to other months during a year.

2. For the total campaigns, almost 61% were successful, 36 % failed and 2.7% canceled.

3. Cancelled campaigns are almost negligible against total launched columns.

- What can you conclude about the Outcomes based on Goals?

1. We can inference that the lower the goal, greater is the probability of success, with an exception of Goal range $35,000 - $50,000
i.e. Goal is inversely proportional to success/performance.

2. Failure has a directly proportional relationship. Higher the Goal, higher chances of failure as an outcome.

3. Optimal range for most successful campaigns is $1000 to $4999 where most campaigns were launched ad a good percentage which is 73% were successful which quite a fair percentage.

- What are some limitations of this dataset?

Limitations of Kickstarter Data set:
There are additional parameters which may provide valuable information to deepen our analysis such as purpose of fundraising, age groups of backers, method of pledging such as online or in-person.

- What are some other possible tables and/or graphs that we could create?
We can create additional tables or graphs that could depict :
1. Relationship between demographics vs use of funds for benefit of local or global community
2. Income group wise backers and their frequency of participation
3. We could depict comparativley better visualization if we take into consideration , duration of campaign, instead of only start dates for outcomes.
