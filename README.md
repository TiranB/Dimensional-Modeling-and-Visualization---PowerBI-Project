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
       - split columns/remove duplicate values/replace values/ Add index columns/ Merge tables

   2. Create Date dimension table
       -we cannot create a date table directly by using dates column in the sales table because it can have gaps between dates.
       -The date table was created using a query.
      
   3. Check the created Model for accurate relatioships in the Model view.

Objective 2 - Create Interactive Visualizations
       Page 1 - Sales by Products
                       * Cards for Total Sales, Total orders, Total cost , Total profit, Average rating (Filtered by Category of product)
                       * Stacked Bar Chart for Top 10 products by sales ( Drill through to page 2 which shows the sales for chosen products on a Map,
                                                                          Drill through to page 3 which shows the sales in each month and year for chosen product on a Matrix
                                                                          Drill in to show the Total sales for chosen product for the sale years in a bar chart)
                       * Decomposition Tree to show average rating for each category and their respective products, descending order.
                       *Treemap to show top 5 best selling products in May 2015 (Highest achieved sales month)
      Page 2 - State - Drilled field for 1st page
      Page 3 - Timeline - Drilled field for 1st page
      Page 4 - Sales by Dates
                      * Ribbon chart to show most popular products over time. (2014-2015 Highest achieved sales years)
                      * Line and stacked column chart to show the Budget sales and the Actual sales. (filter for category-segment)
                      * Stacked Bar chart to show the 'sales by day of the week'. (drill in to see the top 5 products sold in each days)
      Page 5 - Location details
                      * Filled Map of USA to show three sales attributes (sales volume, units sold, earned profit) in each state of the country using a tool tip mapped to page 5.
                      * Map of USA to show the number of customers by each state.
      Page 5 - Tooltip page for Filled Map in page 5.
      
      

        


      

      
