

**Hotel Revenue analysis using SQL and Power BI**

The main aim of this project is to build a visual data story and dashboard using power BI to present to the Hotel stakeholders to specifically answer the following business question.

1.	Is the hotel revenue growing by year?
2.	Should the Hotel increase the parking lot spaces
3.	What other trends can be seen in the data that will be of interest to stakeholders.

  ** Data**
  
The dataset used for this project is an excel file consisting of five tables. The first three tables consist of the hotels records for the year 2018, 2019 and 2020 with 21,992, 79,260, and 69,056 records respectively. The fourth table consist of information for the meal cost in the hotel while the fifth table contains information on the market segment served by the hotel.


**The project Pipeline**

	**Build a database**
I created a database using the Microsoft SQL Server Management Studio and the hotel data was uploaded into the database.

**	Develop the SQL query**
I developed a first SQL query to join the tables containing the hotel record for the years 2018. 2019 and 2020 using the following query:

with hotels as (
select *from dbo.['2018$']
union
select *from dbo.['2019$']
union
select *from dbo.['2020$'])

The second query I developed was to carry out a left joins of the meal cost and market segments to the hotels table before using advanced options to connect the resulting table into power BI for further analysis. The following SQL query was developed:
with hotels as (
select *from dbo.['2018$']
union
select *from dbo.['2019$']
union
select *from dbo.['2020$'])

Select *from hotels
left join dbo.market_segment$
on hotels.market_segment= market_segment$.market_segment
left join dbo.meal_cost$
on meal_cost$.meal=hotels.meal

**	Connect power BI to the Database**

I connected the resulting table with power BI with my server name and using the advanced option of placing the SQL query above into the import wizard of power BI

**	Visualize the Data**
The data was visualized in power BI desktop to answer the business questions that are of particular interest to the hotel stakeholders.

	Summary of Findings

1. The hotel Revenue  is growing by year
2. No evidence to show the need to increase parking space
3. Night bookings is also increasing by year







