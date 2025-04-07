This project demonstrates the transformation of raw, flat sales and budget data  into well-structured dimensional data model using Power BI. The primary objective is to design an efficient Snowflake schema to improve data 
organization and enhances performance for analytical queries. The secondary objective is to create meaningful and interactive visualizations to derive insights from data. 

Data Model Overview :-

  Fact Tables
      1. FactSales - capture the ordered sales data
      2. FactBudget - holds forecasted and budgeted sales data

  Dimension Tables
      1.DimCustomer - customer info
      2.DimProduct  - product info
      3.DimGeography - customer's Geo-location info
      4.DimDate - Sale date info
      5.DimCatSeg - product category-segment info

Objective 1 - Design Dimensional Data Model

   1. Clean and transform the flat data in Power Query Editor
       - duplicate the flat table to create dimension tables.
       - remove unnecessary columns from respective table
       - split columns/remove duplicate values/replace values

   2. Create Date dimension table
       -we cannot create a date table directly by using dates column in the sales table because it can have gaps between dates.
