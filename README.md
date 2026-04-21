# end-to-end-finance-analytics-pipeline
End-to-end finance analytics platform built with DuckDB, Python, and SQL. Implements medallion architecture (Bronze/Silver/Gold), P&amp;L data modeling, and scenario analysis. Integrates with Power BI for executive dashboards, KPI monitoring, and data-driven financial decision-making.

# 📊 Finance Analytics Platform (DuckDB + Power BI)

An end-to-end finance analytics solution that transforms raw General Ledger (GL) data into a structured P&L model, enabling KPI tracking, scenario analysis, and executive reporting.

Built using a modern medallion architecture (Bronze → Silver → Gold) and designed for scalability, data quality, and business alignment.

---

## 🚀 Project Overview

This project simulates a real-world finance analytics environment where raw accounting data is ingested, cleaned, modeled, and exposed for business intelligence.

Key outcomes:

- Standardized P&L reporting structure
- Enabled monthly financial analysis
- Built scenario modeling (Best/Worst case)
- Prepared data for Power BI dashboards

---

## 🏗️ Architecture
Raw Data Sources (Excel + GL Tables)
        ↓
Bronze Layer (Raw Ingestion)
        ↓
Silver Layer (Data Cleaning & Standardization)
        ↓
Gold Layer (Business-Ready Data Model)
        ↓
Power BI (KPIs & Dashboards)


--- 

## 🧱 Data Model
🔹 Fact Tables
- gold__fact_gl_transactions
- gold__fact_gl_transactions_monthly
- gold__adv_fact_gl_scenarios
🔹 Dimension Tables
- gold__dim_account_mapping
- gold__accounts
- gold__dim_stores
- Date dimension (Power BI)

---

## 💼 Business Use Case

The project models a Finance Department use case:

- Transform GL transactions into a structured P&L
- Align accounting data with reporting standard
  
Provide visibility into:
     - Revenue
     - Cost of Goods Sold (COGS)
     - Operating Expenses
     - Financial Items

---

📊 Key Features
- ✅ Medallion Architecture
Clear separation of raw, cleaned, and business-ready data
- ✅ Data Quality & Standardization
Type casting, trimming, normalization
Resolution of mapping inconsistencies from finance stakeholders
- ✅ P&L Mapping Logic
Account-level classification into:
Revenue
COGS
Operating Expenses
Financial Items
- ✅ Monthly Aggregation
Time-based financial reporting using DATE_TRUNC
- ✅ Scenario Analysis
Actual vs Best Case vs Worst Case
Simulates financial sensitivity:
Revenue ↑ / ↓
Cost optimization / inflation
