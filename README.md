# Grind Sales & Pricing Analytics ☕ 📈

An end-to-end data engineering and business intelligence project that consolidates three years of retail transaction data into a high-performance analytical dashboard. This project automates data cleaning, performs complex joins, and visualizes key financial metrics to drive retail strategy.

## 📌 Overview
This project transforms fragmented yearly sales data into a unified "Single Source of Truth." By leveraging SQL for ETL (Extract, Transform, Load) and Power BI for visualization, the system provides a comprehensive view of revenue, profit margins, and regional performance across a three-year timeline (2023–2025).

## ⚠️ The Problem: "Fragmented Data & Financial Gaps"
Retail datasets are often siloed by year, making long-term growth analysis difficult. Furthermore, missing revenue entries can lead to skewed financial reports. This project addresses these issues by:
*   **Unifying Silos:** Merging multi-year tables into a continuous stream.
*   **Data Integrity:** Implementing a fallback logic to calculate missing revenue based on master product pricing.

## ✨ Features
*   **Multi-Year Data Consolidation:** Uses SQL Common Table Expressions (CTEs) and `UNION ALL` to bridge data from 2023, 2024, and 2025.
*   **Automated Revenue Recovery:** Employs `CASE` logic to automatically calculate `CleanedRevenue` (Price * Quantity) if the original revenue field is null.
*   **Weekly Trend Tracking:** Generates a standardized `Week_Date` for time-series analysis using `DATEADD` and `DATEDIFF` functions.
*   **Profitability Analytics:** Joins transactional data with product metadata to calculate real-time Profit and Cost of Goods Sold (COGS).
*   **Interactive Executive Interface:** As seen in **Screenshot 2026-05-09 at 5.14.10 PM.jpg**, the dashboard tracks 1.563K total customers and a 55.06% average margin.

## 🛠 Tech Stack
*   **Database:** SQL (TSQL) for data transformation and cleaning.
*   **Visualization:** Power BI / Interactive Dashboard.
*   **Logic:** CTEs, Left Joins, Conditional Logic, and Vectorized Date Math.

## 🏗 Data Pipeline Architecture
The system follows a three-stage transformation logic:
1.  **Consolidation:** Stacks yearly tables into a single `all_orders` CTE.
2.  **Enrichment:** Joins the unified orders with `customers` and `products` tables to add regional and category context.
3.  **Refinement:** Calculates profit margins, cleans null revenue, and filters for valid customer IDs to ensure report accuracy.

## 📂 Project Structure
*   **SQL Script:** The core logic for data cleaning, joining, and metric calculation.
*   **Dashboard (Screenshot 2026-05-09 at 5.14.10 PM.jpg):** An interactive UI featuring:
    *   **High-Level KPIs:** Total Revenue ($309.34K) and Total Profit ($170.22K).
    *   **Product Performance:** A breakdown of categories including Subscriptions, Consumables, and Hardware.
    *   **Regional KPI Heatmap:** A weekly trend analysis comparing the North, South, East, and West regions.

## 🚀 Impact
This tool allows retail stakeholders to pivot from reactive tracking to proactive management. By identifying that **Grinders & Brewers** and **Subscriptions** drive significant portions of the **$170.22K profit**, the business can optimize pricing and inventory strategies for 2026.

## 👤 Contact
**Project Lead:** Soha Momin  
**Email:** msoha28@my.yorku.ca
