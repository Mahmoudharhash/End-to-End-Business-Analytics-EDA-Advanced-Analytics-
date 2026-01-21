# End-to-End Business Analytics Using Gold Layer

## Overview
This repository demonstrates an end-to-end analytics framework built on top of a **Data Warehouse Gold Layer**.

The project shows how a single, well-designed Gold Layer can power:
- Exploratory Data Analysis (EDA)
- Advanced Business Analytics
- Customer & Product Analytical Reports
- Business-ready KPIs suitable for BI dashboards

The entire workflow is SQL-driven and focuses on **scalability, reusability, and business impact**.

---

## Data Architecture
The project follows the **Bronze / Silver / Gold** data warehousing architecture:

### Bronze Layer
- Raw data ingestion
- Minimal transformation
- Source-aligned tables

### Silver Layer
- Cleaned and standardized data
- Business logic applied
- Data quality handling

### Gold Layer
- Analytical views
- Optimized for reporting and analysis
- Single source of truth for insights

---

## Repository Structure
01_data_warehouse/
├── bronze/
├── silver/
└── gold/

02_eda/
├── 01_dimensions_exploration.sql
├── 02_date_range_exploration.sql
├── 03_measures_exploration.sql
├── 04_magnitude_analysis.sql
└── 05_ranking_analysis.sql

03_advanced_analytics/
├── 01_change_over_time.sql
├── 02_cumulative_analysis.sql
├── 03_performance_analysis.sql
├── 04_data_segmentation.sql
├── 05_part_to_whole.sql
├── 06_customer_report.sql
└── 07_product_report.sql


---

## Exploratory Data Analysis (EDA)
This module focuses on understanding the data and overall business performance.

### Key Analyses
- Dimension exploration:
  - Countries
  - Categories, subcategories, products
- Date range analysis:
  - First and last order date
  - Business duration
  - Youngest and oldest customers
- Core KPIs:
  - Total Sales
  - Total Orders
  - Total Customers
  - Total Products
  - Average Selling Price
- Magnitude analysis:
  - Customers by country and gender
  - Products and revenue by category
- Ranking analysis using window functions:
  - Top 5 products by revenue
  - Worst-performing products
  - Top 10 customers by revenue
  - Customers with the fewest orders

---

## Advanced Analytics
This module transforms descriptive insights into decision-support analytics.

### Key Analyses
- Change-over-time analysis using `DATETRUNC()` and `FORMAT()`
- Cumulative and running total analysis
- Performance analysis:
  - Year-over-year product performance
  - Comparison vs product historical averages
- Data segmentation:
  - Product segmentation by cost and revenue
  - Customer segmentation:
    - VIP: lifespan ≥ 12 months & total sales > 5,000
    - Regular: lifespan ≥ 12 months & total sales ≤ 5,000
    - New: lifespan < 12 months
- Part-to-whole analysis:
  - Category contribution to total sales

---

## Analytical Reports

### Customer Report
A consolidated customer-level analytical view designed for BI consumption.

Includes:
- Customer demographics and age groups
- Customer segmentation (VIP / Regular / New)
- Aggregated metrics:
  - Total orders
  - Total sales
  - Total quantity purchased
  - Total products
  - Customer lifespan (months)
- KPIs:
  - Recency (months since last order)
  - Average Order Value (AOV)
  - Average Monthly Spend

---

### Product Report
A consolidated product-level analytical view.

Includes:
- Product attributes (category, subcategory, cost)
- Revenue-based segmentation:
  - High Performers
  - Mid-Range
  - Low Performers
- Aggregated metrics:
  - Total orders
  - Total sales
  - Total quantity sold
  - Unique customers
  - Product lifespan (months)
- KPIs:
  - Recency (months since last sale)
  - Average Order Revenue (AOR)
  - Average Monthly Revenue

---

## Tools & Technologies
- SQL Server
- T-SQL
- Data Warehousing (Bronze / Silver / Gold Architecture)

---

## Business Value
- Converts raw data into decision-ready insights
- Enables multiple analytical use cases from a single Gold Layer
- Designed to feed BI tools such as Power BI or Tableau
- Supports data-driven decisions across sales, marketing, and product teams

---

## Future Enhancements
- Power BI dashboards on top of Gold views
- Query performance optimization
- Advanced customer analytics (RFM / Cohort Analysis)
