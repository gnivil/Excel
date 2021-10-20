# Excel Challenge - KickStart My Chart
Over $2 billion has been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Of the more than 300,000 projects launched on Kickstarter, only a third have made it through the funding process with a positive outcome.

Getting funded on Kickstarter requires meeting or exceeding the project's initial goal, so many organizations spend months looking through past projects in an attempt to discover some trick for finding success. For this week's homework, you will organize and analyze a database of 4,000 past projects in order to uncover any hidden trends.

-----

# Analysis
* Modified and analysized dataset of 4,000 past Kickstarter projects to uncover some market trends.
* Used conditional formatting to fill each cell in the state column with a different color, depending on whether the associated campaign was successful, failed, or canceled, or is currently live.
* Created a new column O called 'Percent Funded' that uses the divide formula to uncover how much money a campaign made to reach its initial goal.
* Used conditional formatting to fill each cell in the 'Percent Funded' column using a three-color scale. The scale starts at 0 with a dark shade of red, transitioning to green at 100, and blue at 200.
* Created a new column P called 'Average Donation' that uses the Average formula to uncover how much each backer for the project paid on average.
* Created two new columns, one called 'Category' at Q and another called 'Sub-Category' at R, which use Left and Right Find formulas to split the 'Category and Sub-Category' column into two parts.
* Created a new column named 'Date Created Conversion' that uses the Unix timestamps formula to convert the data contained within 'launched_at' into Excel's date format.
* Created a new column named 'Date Ended Conversion' that uses the Unix timestamps formula to convert the data contained within 'deadline' into Excel's date format.

![alt text](https://github.com/gnivil/Excel-Challenge/blob/bbb193e4f608185bcb2273a70c6047426241a801/Chart%20Images/Chart%20Snippet_Kickstart%20My%20Chart.png)

* Created a new sheet with a pivot table analyzing the initial worksheet to count how many campaigns were successful, failed, canceled, or are currently live per 'category'.
* Created a stacked column pivot chart that can be filtered by 'country' based on the pivot table created.

![alt text](https://github.com/gnivil/Excel-Challenge/blob/bbb193e4f608185bcb2273a70c6047426241a801/Chart%20Images/Category%20Breakdown_Kickstart%20My%20Chart.png)

* Created a new sheet with a pivot table analyzing initial worksheet to count how many campaigns were successful, failed, or canceled, or are currently live per 'sub-category'.
* Created a stacked column pivot chart that can be filtered by 'country' and 'parent-category' based on the pivot-table created.

![alt text](https://github.com/gnivil/Excel-Challenge/blob/bbb193e4f608185bcb2273a70c6047426241a801/Chart%20Images/Subcategory%20Breakdown_Kickstart%20My%20Chart.png)

* Created a new sheet with a pivot table with a column of 'state', rows of 'Date Created Conversion', values based on the count of 'state', and filters based on 'parent category' and 'Years'.
* Created a pivot chart line graph that visualizes the pivot-table created.

![alt text](https://github.com/gnivil/Excel-Challenge/blob/bbb193e4f608185bcb2273a70c6047426241a801/Chart%20Images/Monthly%20Breakdown_Kickstart%20My%20Chart.png)

-----

# Bonus
* Created a new sheet with 8 columns:
    * Goal
    * Number Successful
    * Number Failed
    * Number Canceled
    * Total Projects
    * Percentage Successful
    * Percentage Failed
    * Percentage Canceled
* In the 'Goal' column, create 12 rows with the following headers:
    * Less than 1000
    * 1000 to 4999
    * 5000 to 9999
    * 10000 to 14999
    * 15000 to 19999
    * 20000 to 24999
    * 25000 to 29999
    * 30000 to 34999
    * 35000 to 39999
    * 40000 to 44999
    * 45000 to 49999
    * Greater than or equal to 50000
* Using the COUNTIFS() formula, counted how many successful, failed, and canceled projects were created with goals within the ranges listed above. Populated the 'Number Successful', 'Number Failed', and 'Number Canceled' columns with this data.
* Added up each of the values in the 'Number Successful', 'Number Failed', and 'Number Canceled' columns to populate the 'Total Projects' column. Then, calculated the percentage of projects that were successful, failed, or canceled per goal range.
* Created a line chart that graphs the relationship between a goal's amount and its chances at success, failure, or cancellation.

![alt text](https://github.com/gnivil/Excel-Challenge/blob/bbb193e4f608185bcb2273a70c6047426241a801/Chart%20Images/Bonus_Kickstart%20My%20Chart.png)

-----

# Bonus Statistical Analysis
* Created a new worksheet in the workbook, and created a column each for the number of backers of successful campaigns and unsuccessful campaigns.
* Used Excel to evaluate the following for successful and unsuccessful campaigns:
    * The mean number of backers
    * The median number of backers.
    * The minimum number of backers.
    * The maximum number of backers.
    * The variance of the number of backers.
    * The standard deviation of the number of backers.

![alt text](https://github.com/gnivil/Excel-Challenge/blob/bbb193e4f608185bcb2273a70c6047426241a801/Chart%20Images/Bonus%20Statistical%20Analysis_Kickstart%20My%20Chart.png)

-----

# Written Analysis
## Kickstart My Chart Report
* Given the provided data, what are three conclusions we can draw about Kickstarter campaigns?
    * Kickstarter campaigns in the Music category are the most prevalent with 1393 campaigns run and 60.22% of them ending successfully.
    * The most successful Kickstarter campaigns were in the music category with a success rate of 77.14%.
    * Technology Kickstarter campaigns have a success rate of 34.83% despite having the highest backing of 174,797 people.

* What are some limitations of this dataset?
    * The data is sourced from around the world, and it is unclear how the currency value was normalized.
    * Two technology, one music, and one games campaigns all have upper-bound outliers.
    * We only analyze 4,000 of the 300,000 Kickstarter campaigns.

* What are some other possible tables and/or graphs that we could create?
    * Visualize the backers count data by category.
    * Compare the state of Kickstarter campaigns by country.
    * Analyze monthly breakdown of the state of Kickstarter campaigns, excluding data for campaigns in the theater category since they disproportionately represent the dataset.

## Bonus Statistical Analysis Report
* Does the mean or the median summarize the data more meaningfully?
The Median summarizes the data more meaningfully because the data is slightly skewed due to outliers.

* Is there more variability with successful or unsuccessful campaigns? Does this make sense? Why or why not?
There is more variability with successful campaigns. This makes sense because there were four campaigns that had upper-bound outliers skewing the dataset, thus increasing its variance.

-----
