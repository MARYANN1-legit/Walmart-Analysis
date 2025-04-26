# Walmart-Analysis
One of the leading retail stores in the US, Walmart, would like to predict the sales and demand accurately. There are certain events and holidays which impact sales on each day. There are sales data available for 45 stores of Walmart. Analyzing the challenges, unforeseen demands and factors that can affect this sales.

### DATA SOURCE
The dataset is taken from Kaggle.

### Tool used
- Excel : Data Cleaning
- SQL Server : Data Analysis
- Power BI : Data Visualization

### Data Cleaning
Data cleaning and pre-processing were carried out at the initial stage to ensure the quality of data
Thus;
- Data loading and inspection
- Handling duplicates
- fixing the un-standardized date format
-  Changing the formats of some columns

-  ### Exploratory data analysis (EDA)
The EDA process involves understanding data, identifying patterns and detecting anomalies to inform futher analysis(like answering key questions)
1. -- Sales trend?
2. --Effect of fuel price on weekly sales?
3. --Impact on holidays on weekly sales?
4. --Effect of CPI on weekly_sales?


### DATA Analysis
Data analysis was done in SQL

~~~
-- sales trend


select top 10 Store, Date, AVG(weekly_sales) AS  sales_by_week
from [Walmart p2]
group by store, date order by sales_by_week DESC;

--Effect of fuel price on weekly sales

select fuel_price, date,sum(weekly_sales) as weekly_sales
from [Walmart p2]
group by Fuel_Price, date
order by weekly_sales DESC

--impact on holidays on weekly sales

select Holiday_Flag, AVG(weekly_sales) as average_sales
from [Walmart p2]
group by holiday_flag;

--EFFECT OF CPI ON WEEKLY SALES
SELECT CPI, SUM(WEEKLY_SALES) AS TOTAL_SALES
FROM [Walmart p2]
GROUP BY CPI
~~~


### Results/FINDINGS
Sales Trend
- Sales have been decreasing over time, with a sales growth rate of -18.30%.
- Total sales amount to $6.2 billion.

Holiday Sales
- Holidays positively impact weekly sales, with $505,229,551 in sales during holidays.

Pricing and CPI Analysis
- Fair price has no significant effect on weekly sales.
- Consumer Price Index (CPI) has a minor effect on weekly sales.
- 
### Recommendations
1. Optimize sales strategies: Identify reasons for declining sales and adjust strategies to reverse the trend.
2. Leverage holidays: Capitalize on holidays to boost sales, considering successful past promotions.
3. Monitor CPI impact: Keep a close eye on CPI's effect on sales and adjust pricing strategies accordingly.
   
### Limitations


