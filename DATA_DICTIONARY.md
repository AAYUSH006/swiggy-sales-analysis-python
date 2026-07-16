# Data Dictionary

## Overview

This document describes the fields present in the **Swiggy Sales Analysis** dataset used for exploratory data analysis and business insight generation.

**Dataset Summary**

| Attribute | Value |
|----------|------:|
| Total Records | 197,430 |
| Total Columns | 10 |
| Data Type | Structured |
| Format | Microsoft Excel (.xlsx) |

---

## Column Definitions

| Column Name | Data Type | Description | Example |
|-------------|-----------|-------------|---------|
| **State** | Text | Indian state where the restaurant is located. | Karnataka |
| **City** | Text | City in which the restaurant operates. | Bengaluru |
| **Order Date** | Date | Date associated with the order record. | 29-06-2025 |
| **Restaurant Name** | Text | Name of the restaurant offering the dish. | Anand Sweets & Savouries |
| **Location** | Text | Locality or neighborhood of the restaurant. | Rajarajeshwari Nagar |
| **Category** | Text | Menu category under which the dish is listed. | Snack |
| **Dish Name** | Text | Name of the food item. | Butter Murukku-200gm |
| **Price (INR)** | Decimal | Selling price of the dish in Indian Rupees (₹). | 133.90 |
| **Rating** | Decimal | Average customer rating on a 5-point scale. | 4.0 |
| **Rating Count** | Integer | Total number of customer ratings received for the dish. | 0 |

---

## Data Types

| Data Type | Columns |
|-----------|---------|
| **Text (Object)** | State, City, Restaurant Name, Location, Category, Dish Name |
| **DateTime** | Order Date |
| **Float** | Price (INR), Rating |
| **Integer** | Rating Count |

---

## Key Business Metrics Derived

During the analysis, additional features were created to support business reporting.

| Derived Feature | Description |
|-----------------|-------------|
| **YearMonth** | Month-Year extracted from Order Date for monthly sales trend analysis. |
| **DayName** | Day of the week extracted from Order Date for weekday revenue analysis. |
| **Quarter** | Financial quarter derived from Order Date for quarterly performance analysis. |
| **Food Category** | Classification of dishes into **Veg** and **Non-Veg** using keyword-based text analysis. |

---

## Data Quality Notes

- Order Date was converted to **DateTime** format for time-series analysis.
- No missing values were identified in the primary analytical columns.
- Numerical fields such as **Price (INR)** and **Rating** were validated before KPI calculations.
- Additional derived columns were created without modifying the original dataset.

---

## Purpose

This dataset is used to analyze:

- Sales performance
- Customer ratings
- Restaurant performance
- State-wise revenue
- Monthly and quarterly trends
- Veg vs Non-Veg revenue contribution
- Business KPIs through Python-based exploratory data analysis
