# 📊 Small Retail Business — Sales Performance Dashboard

## 📝 Project Objective
The goal of this project was to analyze synthetic sales data for a US & UK-based retail business, execute end-to-end data cleaning, and build a fully interactive Excel dashboard to track Key Performance Indicators (KPIs), regional performance, and product trends. 

### 🚀 The Final Dashboard
*(Note: Click to enlarge)*
![Sales Dashboard](https://github.com/user-attachments/assets/74a6f738-27a1-42fb-9c21-5ec62cdbb72b)

## 🗂️ Dataset Details
- **Total Records:** 650 raw rows (645 unique after cleaning).
- **Timeframe:** January 2025 to October 2026.
- **Dimensions tracked:** 18 columns including Order Date, Region, Sales Channel, Customer Segment, Product Category, and Order Status.

## 🛠️ Methodology (The Analytics Process)
This project was executed in a structured analytics pipeline:

### 1. Data Cleaning
- **Deduplication:** Identified and removed 5 fully duplicated transaction records that would have artificially inflated revenue.
- **Handling Missing Values:** Applied logical overrides for missing `Ship_Date` values, as these were exclusively tied to `Cancelled` orders.
- **Text Standardization:** Utilized the `PROPER()` function to fix inconsistent text capitalization across `City` and `Sales_Channel` dimensions.

### 2. Data Modeling (Calculated Columns)
Modeled the financials by building the following calculated columns:
- **Gross Sales:** `Quantity * Unit Price`
- **Discount Amount:** `Gross Sales * Discount Rate`
- **Net Sales:** `Gross Sales - Discount Amount`
- **Total Cost:** `Quantity * Unit Cost`
- **Estimated Gross Profit:** `Net Sales - Total Cost`

### 3. PivotTables & Data Aggregation
Created a multi-sheet architecture (`Trends`, `Category`, `Region`) using PivotTables. Applied filters to ensure **only "Completed" orders** contributed to the final revenue KPIs, isolating "Returned" and "Cancelled" orders for separate analysis. 

## 💡 Key Business Insights

1. **Electronics & Web Traffic Dominate:** The Electronics category is the overwhelming revenue leader, with "Smart Watch" and "Wireless Earbuds" acting as the flagship products. Furthermore, the **Website** significantly outperforms Marketplaces and Retail Stores as the primary sales channel.
2. **Geographical Stronghold:** The **US-East** region generates the highest total revenue, indicating strong brand penetration on the East Coast compared to UK and Western US markets.
3. **Critical Profit Leak (16.5% Return Rate):** Out of the 645 unique orders, 107 were returned. The 16.5% return rate highlights a potential profitability and operational risk that warrants further investigation.

## 🎯 Strategic Recommendations
- **Reallocate Marketing Spend:** Consider reallocating part of the marketing budget from Retail Stores toward the Website channel, subject to profitability and customer-acquisition-cost validation and funnel it into targeted digital ads for Tech/Electronics products on the US East Coast.
- **Investigate the Return Pipeline:** The operations team must immediately investigate why items are being returned. Improving product descriptions, sizing charts, or quality control could instantly recapture thousands of dollars in lost profit.

## 💻 Tech Stack Used
- **WPS Office Sheets** (Data Cleaning, Formulas, PivotTables, PivotCharts, Slicers, Dashboard Design)
