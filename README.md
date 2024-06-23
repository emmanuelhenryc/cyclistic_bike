
# Cyclistic Bike Analysis


## Table Of Content


- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
-	[Data Cleaning/Preparation](#data-cleaningpreparation)
-	[Exploratory Data Analysis](#exploratory-data-analysis)
-	[Data Analysis](#data-analysis)
-	[Result/Findings](result/findings)
-	[Recommendations](#recommendations)


## Project Overview
Analysis on Cyclistic bike aim to provide insights into the uses of bikes by two customer types. By analyzing various aspect of the bike data, we aim at identifying trends on how member and casual riders use bike differently, make data-driven recommendations, and gain a deeper understanding of the company’s performance.

## Data Sources
Bike data: The datasets used for this analysis is the “2022-divvytripdata.csv” file for each month of January – December, containing detailed information of bike riders and their hire type.
Data can be found here -- https://drive.google.com/file/d/1VP8VOcp0LFnepUN02Ff7YDAs-KFM7O3O/view?usp=drive_link

## Tools
- Excel – Data Cleaning 
  -	[Download_here](https://microsoft.com)
- SQL Server – Data Analysis
- PowerBI – Creating reports

## Data Cleaning/Preparation
For data preparation and processing phase, the following tasks was performed:
1. Data stacking, loading and inspection.
2. Handling missing values.
3. Data Cleaning and formatting

## Exploratory Data Analysis
EDA involves exploring the sales data to answer key questions, such as:

- How many minutes averagely do members and casuals spend on a bike?
- Which bike is mostly used by members and casuals?
- Which year quarter(s) has the highest bike hire?

EDA was done using SQL. It can be found in the code section. 
## Data Analysis

```sql
select customer_type, month_hire, avg(mins_hire) as average_minutes
from cyclistic_trans_2022
where ride_type = 'classic_bike' or ride_type = 'electric_bike'
group by month_hire, customer_type
order by average_minutes desc
```

## Result/Findings
The analysis results are summarized as follows:
1. Annual members and casual riders hire bikes majorly in the second and third quarter of the year.
2. Members use either of classic or electric bikes, Casual riders use either of classic, electric, or docked bikes.
3. Casual riders increase as the week progresses from Sunday to Friday, with a decrease from Friday to Saturday.
4. Annual members increase on the first to second day of the week and decrease as the week progresses.
5. Casual riders spend more time averagely with a bike as compared to members.
6. Annual members use classic bike mostly, casual riders use electric bike mostly.

## Recommendations
Based on the analysis, we recommend the following actions to convert casual riders to annual members:
-	Ads on membership should be delivered via electric and docked bikes mostly.
-	Membership marketing/awareness should be done mostly on Saturday, Sunday, and Monday.
- Casual riders use bikes mostly on June, July and August. Discount should be given to only "members"(annual) on these momths in order to catch the attention of casual riders and possibly get them to register to become a member in order to be able to receive discounts. 


   




