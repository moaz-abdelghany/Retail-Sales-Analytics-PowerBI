# Power Query Documentation

## Overview

This document describes the ETL (Extract, Transform, Load) process used to prepare the retail sales dataset before building the Power BI data model and dashboards.

---

# 1. Dim_Customers

### Source
- Imported the raw customer dataset.
- Verified and assigned appropriate data types.

### Transformations
- Merged **First Name** and **Last Name** into a new **Full Name** column.
- Calculated **Customer Age** from Birth Date.
- Created **Age Group** categories.
- Calculated **Loyalty Years** using Join Date.
- Created **Loyalty Tier** (Bronze, Silver, Gold) using conditional logic.

---

# 2. Dim_Products

### Source
- Imported product data.
- Applied correct data types.

### Transformations
- Calculated **Unit Profit**

```
Unit Profit = Unit Price - Cost Price
```

- Calculated **Unit Profit Margin (%)**

```
Unit Profit Margin = Unit Profit / Unit Price
```

---

# 3. Dim_Stores

### Source
- Imported store data.
- Validated Store IDs and text columns.

### Transformations
- Applied **Trim**.
- Applied **Clean**.
- Standardized **City** and **Region** values.

---

# 4. Fact_Transactions

### Source
- Imported transaction table (5,000 records).

### Transformations

Calculated **Gross Sales**

```
Gross Sales = Unit Price × Quantity
```

Calculated **Discount Amount**

```
Discount Amount = Gross Sales × Discount
```

Calculated **Revenue**

```
Revenue = Gross Sales − Discount Amount
```

Calculated **Total Cost**

```
Total Cost = Cost Price × Quantity
```

---

# 5. Dim_Date

### Source

Generated a dynamic calendar table based on the minimum and maximum transaction dates.

### Transformations

Added:

- Year
- Quarter
- Month Number
- Month Name

---

# ETL Summary

The Power Query workflow included:

- Data Extraction
- Data Cleaning
- Data Transformation
- Feature Engineering
- Dynamic Date Table Creation
- Data Loading

The prepared tables were then used to build a Star Schema data model in Power BI for DAX calculations and dashboard development.