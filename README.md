# LITA-Capstone-Project 1

This is one of the projects done after completing the Data Analysis program with the Incubator Hub.

### Project Title: Sales Performance Analysis for a Retail Store
---
### Content
---
[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning and Preparation](#data-cleaning-and-preparation)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis) 

[Data Visualisation](#data-visualisation)


### Project Overview
---
This project aims to generate an insight into the sales performance of a retail store over some given period. The analysis begins with an exploration of sales data using Excel, where pivot tables are utilized to summarize total sales by product, region, and month. Key metrics, including average sales per product and total revenue by region, are calculated using Excel formulas. Additionally, supplementary reports are created to highlight any other interesting findings. The culmination of this analysis is an interactive Power BI dashboard that visually presents top-selling products, regional performance, and monthly sales trends, enabling stakeholders to make informed decisions based on the data.
### Data Sources
---
The primary source of Data used for this project is Sale Data.csv, which is open-source data that can be freely downloaded from sites such as Kaggle, FRED, or any other data repository site.

### Tools Used
---
- Microsoft Excel [Download Here](https://www.microsoft.com)
  1. For Data cleaning
  2. For Analysing
  3. Visualisation

- SQL - Structured Query Language for querying of Data
- PowerBI for Data modeling
- GitHub  for Portfolio Building.

### Data Cleaning and Preparation
---
In the initial phase of the Data cleaning and preparation, we perform the following actions:
1. Data loading and inspection
2. Handling missing variables
3. Data cleaning and formatting

### Exploratory Data Analysis
---
EDA involves the exploration of the Data to answer some questions about the Data such as:
- What is the overall sales trend
- Which products are top sellers
- What are the products on the peak sales

### Data Analysis
---
This is where we include some basic lines of code or queries or even some of the DAX expressions used during the analysis

Pivot Table: Sorting Transactions by Category into Low, Medium, and High

```Pivot Table
=IF(G12610<20,"Low",IF(G12610<=50,"Medium","High"))
```

Excel Formula for Average Sales per Product

```Excel Table
=AVERAGEIF(C2:C50001,C2,G2:G50001)
```

Total Revenue by Region

```Excel Table
=SUMIF(D2:D50001,D2,G2:G50001)
```

--- Total Number of Customers by Region in SQL ---

```Select * from [dbo].[Customers Data]
Where Region = 'North'
```
```Select Count(*) As NorthCustomers from [dbo].[Customers Data]
Where Region = 'North'
```
```Select Count(*) As EastCustomers from [dbo].[Customers Data]
Where Region = 'East'
```
```Select Count(*) As WestCustomers from [dbo].[Customers Data]
Where Region = 'West'
```
```Select Count(*) As SouthCustomers from [dbo].[Customers Data]
Where Region = 'South'
```
--- Total Number of Active and Canceled Subscribers ---

```Select Count(*) As ActiveSubscription from [dbo].[Customers Data]
Where Canceled = 'FALSE'
```

```Select Count(*) As CanceledSubscription from [dbo].[Customers Data]
Where Canceled = 'TRUE'
```
--- Top 3 Cancelled Region ---

Select top 3 * from [dbo].[Customers Data]
Where Canceled = 'TRUE'



### Data Visualisation
