Pizza Sales Executive Dashboard (Power BI)

An interactive Power BI dashboard analyzing a full year of pizza sales transactions, built on a proper star-schema data model with DAX measures and time-intelligence calculations.

Overview

This project transforms raw transaction-level pizza sales data into an executive-level KPI dashboard with dynamic filtering by category, size, and date range. It covers 49,574 line items across 21,350 orders, spanning January–December 2015.

Data Model

Designed as a star schema for performance and scalability:

Fact_Sales — transaction-level fact table (order ID, date, time, pizza reference, quantity, price)
Dim_Pizza — pizza dimension (name, size, category, price)
Dim_Date — full calendar date dimension (year, month, quarter, weekday, week number), marked as the official Power BI date table to enable time-intelligence functions
Key Metrics (DAX)
Total Revenue — SUMX across quantity × price
Total Orders — DISTINCTCOUNT of order IDs
Average Order Value — revenue divided by distinct orders
Revenue MoM % — month-over-month growth using DATEADD time intelligence
Features
Executive KPI page with color-coded metric cards (Total Revenue, Total Orders, Average Order Value, Total Pizzas Sold)
Monthly Revenue Trend combo chart (bars + growth % line)
Interactive filter panel: Category, Size, and Date range slicers, all cross-filtering the entire page
Custom dark theme with a consistent color system for readability and visual hierarchy
Tools Used
Power BI Desktop (data modeling, DAX, report design)
Power Query (data cleaning and transformation)
Star schema dimensional modeling
Custom Power BI theme (JSON)<img width="1217" height="687" alt="Screenshot 2026-09-03 182659" src="https://github.com/user-attachments/assets/ea551252-1c70-4c8b-a1a6-72a30bb2dfda" />

Files in this Repo
Pizza_Sales_Executive_Dashboard.pbix — the full Power BI report
Fact_Sales.csv, Dim_Pizza.csv, Dim_Date.csv — source data tables
pizza_dashboard_theme.json — custom Power BI theme
screenshots/ — dashboard preview images
