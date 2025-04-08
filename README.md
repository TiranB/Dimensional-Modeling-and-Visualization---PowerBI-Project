# 📊 Power BI Project: Dimensional Modeling and Visualization of Sales & Budget Data

This project demonstrates the transformation of raw, flat **sales and budget data** into a well-structured **dimensional data model** using **Power BI**. The primary objective is to design an efficient **Snowflake Schema** to improve data organization and enhance performance for analytical queries. The secondary objective is to create **meaningful and interactive visualizations** to derive insights from the data.

---

## 🧠 Data Model Overview

### 🔸 Fact Tables

1. **FactSales** – Captures the actual ordered sales data  
2. **FactBudget** – Holds forecasted and budgeted sales data  

### 🔹 Dimension Tables

1. **DimCustomer** – Customer details  
2. **DimProduct** – Product details  
3. **DimGeography** – Customer geographic location  
4. **DimDate** – Date information related to sales  
5. **DimCatSeg** – Product category and segment details  

---

## 🎯 Objective 1 – Design Dimensional Data Model

### 1. Clean and Transform Flat Data Using Power Query Editor

- Duplicated the flat table to create dimension tables  
- Removed unnecessary columns from each table  
- Applied transformations:  
  - Split columns  
  - Removed duplicates  
  - Replaced values  
  - Added index columns  
  - Merged related tables  

### 2. Create Date Dimension Table

- A dedicated `DimDate` table was created using a query  
- A direct date column from sales table was not used due to potential gaps in dates  

### 3. Establish Relationships

- Verified and configured correct relationships between fact and dimension tables using **Model View**

---

## 📈 Objective 2 – Create Interactive Visualizations

### 📄 **Page 1 – Sales by Products**

- **KPI Cards:** *Total Sales*, *Total Orders*, *Total Cost*, *Total Profit*, *Average Rating*  
  *(Filtered by Product Category)*  
- **_Stacked Bar Chart_** – *Top 10 products by sales*  
  - **Drill-through** to:
    - **Page 2:** *Sales by product on a map*  
    - **Page 3:** *Monthly and yearly sales matrix for the selected product*  
    - **Drill-in:** *Year-wise bar chart for total sales*  
- **_Decomposition Tree_** – *Average rating breakdown by category and products (descending)*  
- **_Treemap_** – *Top 5 best-selling products in May 2015 (highest sales month)*

---

### 📄 **Page 2 – State View**

- Visuals for *sales by U.S. state* (from product drill-through on Page 1)

---

### 📄 **Page 3 – Timeline View**

- *Matrix showing sales by month and year* for selected product (from Page 1 drill-through)

---

### 📄 **Page 4 – Sales by Dates**

- **_Ribbon Chart_** – *Most popular products over time (2014–2015)*  
- **_Line & Stacked Column Chart_** – *Budget vs. Actual Sales (with Category-Segment filter)*  
- **_Stacked Bar Chart_** – *Sales by day of the week*  
  - **Drill-in:** *Top 5 products sold on each day*

---

### 📄 **Page 5 – Location Details**

- **_Filled Map of USA_** – Tooltip-based map showing:
  - *Sales Volume*  
  - *Units Sold*  
  - *Profit Earned*  
- **_Map of USA_** – *Number of customers per state*

---

### 🛠 **Tooltip Page (Page 5)**

- Tooltip used in the **_Filled Map_** to show detailed *sales metrics per state*

---

## 🧰 Tools & Technologies

- **Power BI Desktop**
- **Power Query (M Language)**
- **DAX (Data Analysis Expressions)**

---


      
      

        


      

      
