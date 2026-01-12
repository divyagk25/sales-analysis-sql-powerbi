# Sales Analysis Using SQL & Power BI
### End-to-End Business Intelligence Project

---

## Project Overview
This project demonstrates an end-to-end business intelligence workflow
using SQL Server and Power BI. The objective is to transform raw sales
data into meaningful business insights by applying data warehousing
concepts, SQL-based data cleaning, and interactive dashboard design.

The project follows a real-world BI pipeline:
business request → data cleaning → data modeling → visualization.

---

## Business Context
The analysis is based on a business request from stakeholders seeking
insights into:
- sales performance over time
- customer behavior
- product-level revenue trends
- budget vs actual sales comparison

User stories and business demand documents were used to define reporting
requirements before any analysis was performed.

---

## Data Architecture
The project uses a **data warehouse schema** consisting of:

### Fact Table
- **FACT_InternetSales**  
  Contains transactional sales data including revenue, quantity, and dates.

### Dimension Tables
- **DIM_Calendar** – date attributes for time-based analysis  
- **DIM_Customer** – customer demographics and geography  
- **DIM_Product** – product hierarchy and attributes  

This star schema design enables efficient querying and reporting.

---

## Data Cleaning & Transformation (SQL)
Data preparation was performed using **T-SQL** in SQL Server.

Key steps included:
- Cleaning and renaming columns for clarity
- Combining attributes where required
- Handling missing values using `ISNULL()`
- Creating calculated fields using `CASE WHEN`
- Sorting and filtering data using `WHERE` and `ORDER BY`
- Joining fact and dimension tables using `LEFT JOIN`
- Formatting SQL scripts for readability and maintainability

Cleaned datasets were exported as CSV files for use in Power BI.

---

## Power BI Data Modeling
In Power BI:
- Cleaned tables were loaded and validated
- Relationships were defined using a star schema
- A separate **measure table** was created for DAX calculations
- Budget data was imported and linked to sales data

---

## Dashboard Design
The Power BI dashboard was designed to support executive-level decision
making and includes:

- KPI cards for total sales and revenue
- Line charts for sales trends over time
- Bar charts for product and customer performance
- Top 10 products and customers
- Geographic sales distribution using maps
- Budget vs actual comparison
- Interactive filters and slicers


---

## Key Insights
- Sales show strong seasonal patterns over time
- A small group of customers contributes a large share of revenue
- Certain product categories consistently outperform others
- Budget deviations highlight areas requiring business attention

---

## Deliverables
- SQL scripts for data cleaning and transformation
- Cleaned datasets exported from SQL Server
- Interactive Power BI dashboard (`.pbix`)
- Static dashboard preview (`.pdf`)

---

## Repository Structure
```text
sql/           → SQL data cleaning scripts  
data/          → Cleaned and exported datasets  
powerbi/       → Power BI dashboard files  
 
