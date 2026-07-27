# Retail Sales Analytics Dashboard
## Project Walkthrough

---

# Project Overview

The Retail Sales Analytics Dashboard is an end-to-end Business Intelligence project developed using Microsoft Power BI. The project transforms raw retail sales data into an interactive analytics solution that helps decision-makers monitor business performance, evaluate profitability, analyze customer behavior, and identify sales trends.

The solution follows a complete BI workflow starting from data preparation and transformation using Power Query, followed by data modeling with a Star Schema, DAX measure development, and finally interactive dashboard design.

---

# Business Problem

Retail businesses generate thousands of transactions across products, customers, stores, and time periods. Without proper analysis, it becomes difficult to answer important business questions such as:

- How is revenue changing over time?
- Which products generate the highest profit?
- Which categories have the best profit margins?
- How are stores performing?
- Which customer segments generate the highest value?
- Are current business targets being achieved?

The objective of this project is to answer these questions through a dynamic Power BI dashboard.

---

# Project Objectives

The project aims to:

- Monitor overall business performance.
- Track revenue, profit, and sales growth.
- Analyze customer purchasing behavior.
- Evaluate product profitability.
- Compare performance across stores.
- Identify sales trends using Time Intelligence.
- Support management with data-driven decisions.

---

# Dataset Overview

The project analyzes retail sales transactions between **2023 and 2025**.

The dataset includes:

- Customers
- Products
- Stores
- Transactions
- Calendar Table

The final model contains a fact table connected to multiple dimension tables following the Star Schema design.

---

# ETL Process

The dataset was prepared using **Power Query** before building the Power BI model.

Main ETL tasks included:

## Customer Dimension

- Imported customer data.
- Corrected data types.
- Created Full Name.
- Calculated Customer Age.
- Generated Age Groups.
- Calculated Loyalty Years.
- Created Loyalty Tier using conditional logic.

---

## Product Dimension

- Imported product information.
- Corrected data types.
- Calculated Unit Profit.
- Calculated Unit Profit Margin.

---

## Store Dimension

- Imported store information.
- Cleaned text columns.
- Applied Trim and Clean transformations.
- Standardized Region and City values.

---

## Transaction Fact Table

Calculated:

- Gross Sales
- Discount Amount
- Revenue
- Total Cost

These calculations created a clean transactional dataset ready for reporting.

---

## Date Dimension

Created a dynamic calendar table that includes:

- Year
- Quarter
- Month Number
- Month Name

The calendar table enables Time Intelligence calculations across the report.

---

# Data Modeling

The project uses a **Star Schema** model.

The model consists of:

**Fact Table**

- Fact_Transactions

**Dimension Tables**

- Dim_Customers
- Dim_Products
- Dim_Stores
- Dim_Date

This structure improves performance, simplifies relationships, and supports scalable DAX calculations.

---

# DAX Measures

The project includes organized DAX measures grouped using **Display Folders** for easier maintenance.

## Base Measures

- Transactions
- Total Revenue
- Total Gross Sales
- Total Costs
- Total Profit
- Total Discount Amount
- Total Quantity
- Profit Margin %

---

## Average & Rate Measures

- Average Order Value (AOV)
- Average Basket Size
- Average Revenue per Customer
- Average Revenue per Store
- Average Profit per Store
- Average Profit per Order
- Average Loyalty Years
- Average Discount Rate %

---

## Time Intelligence Measures

- Revenue PY
- Profit PY
- Revenue YoY Growth %
- Profit YoY Growth %
- Running Total 2024
- Running Total 2025
- Best Month YoY Growth
- Lowest Month YoY Growth

---

## Product & Ranking Measures

- Top Revenue Category
- Top Profit Category
- Highest Margin Category
- Top Selling Product
- Lowest Product
- Target Profit Margin

---

# Dashboard Walkthrough

## Landing Page

The landing page serves as the entry point of the report and provides navigation to all dashboard pages through an intuitive interface.

---

## Executive Overview

Purpose:

Provide executives with a high-level summary of business performance.

Main KPIs:

- Total Transactions
- Total Revenue
- Total Quantity Sold
- Total Profit
- Profit Margin %

Business Value:

Allows management to quickly understand the overall health of the business before exploring detailed analysis.

---

## Time Intelligence

Purpose:

Analyze business performance over time.

Main KPIs:

- Revenue YoY Growth %
- Profit PY
- Profit YoY Growth %
- Best Month YoY Growth
- Lowest Month YoY Growth

Key Analysis:

- Revenue comparison against Previous Year.
- Profit comparison against Previous Year.
- Monthly performance trends.
- Running Total comparison.
- Growth trend analysis.

Business Value:

Helps identify seasonal trends, monitor business growth, and compare current performance with historical data.

---

## Product Profitability

Purpose:

Evaluate product and category performance.

Main KPIs:

- Top Revenue Category
- Top Profit Category
- Highest Margin Category
- Top Selling Product
- Lowest Product

Business Value:

Supports product portfolio optimization by identifying high-performing and low-performing products.

---

## Sales Performance

Purpose:

Measure sales efficiency.

Main KPIs:

- Transactions
- Revenue
- Quantity Sold
- Average Order Value (AOV)
- Average Basket Size

Business Value:

Provides insights into customer purchasing patterns and overall sales performance.

---

## Customer Analytics

Purpose:

Analyze customer behavior and loyalty.

Main KPIs:

- Total Customers
- Average Revenue per Customer
- Average Discount Rate
- Average Order Value
- Average Loyalty Years

Business Value:

Helps understand customer value, loyalty, and purchasing behavior.

---

## Store Performance

Purpose:

Compare branch performance across different regions.

Main KPIs:

- Total Active Stores
- Number of Regions
- Average Revenue per Store
- Average Profit per Store
- Profit Margin %

Business Value:

Allows management to evaluate branch performance and identify high-performing locations.

---

## Executive Summary

The final dashboard summarizes the overall business performance and presents the project's key findings and recommendations.

---

# Key Business Insights

The analysis highlighted several important findings:

- Revenue demonstrated positive year-over-year growth.
- Profitability remained relatively stable across the reporting period.
- Certain product categories generated significantly higher revenue than others.
- Some categories achieved stronger profit margins despite lower sales volume.
- Customer loyalty played an important role in revenue generation.
- Store performance varied across different regions, highlighting opportunities for operational improvement.

---

# Business Recommendations

Based on the analysis, the following recommendations were identified:

- Invest further in high-performing product categories.
- Improve the performance of low-performing products.
- Expand customer loyalty initiatives.
- Monitor seasonal sales fluctuations.
- Replicate best practices from top-performing stores.
- Continue tracking KPIs through interactive dashboards to support data-driven decision making.

---

# Technical Skills Demonstrated

Throughout this project, the following technical skills were applied:

- Microsoft Power BI
- Microsoft Excel
- Power Query
- Data Cleaning
- ETL (Extract, Transform, Load)
- Data Modeling
- Star Schema
- DAX
- Time Intelligence
- KPI Development
- Dashboard Design
- Business Intelligence
- Data Visualization
- Analytical Thinking
- Business Analysis

---

# Repository Structure

```
Retail-Sales-Analytics/
│
├── Dataset/
├── Excel/
├── Images/
├── Documentation/
│   ├── ETL_Power_Query_Documentation.md
│   └── Project_Walkthrough.md
│
├── Retail_Sales_Dashboard.pbix
├── Retail_Sales_Dashboard.pdf
├── README.md
└── LICENSE
```

---

# Conclusion

This project demonstrates the complete Business Intelligence lifecycle, from raw data preparation and transformation to interactive dashboard development. By combining Power Query, Star Schema modeling, DAX calculations, and business-focused visualizations, the solution provides meaningful insights that support strategic decision-making and performance monitoring.