# Insurance-Customer-value-analysis
Exploratory analysis of auto insurance customer data uncovering key drivers of Customer Lifetime Value and marketing response rates across 9K+ customers.
# 🚗 Auto Insurance Customer Value Analysis

**SQL-driven analysis of 9,000+ auto insurance customers to uncover what drives Customer Lifetime Value (CLV) and marketing response rates — from raw data to an interactive Power BI dashboard.**

---

## 📌 Project Summary

Insurance companies spend heavily on renewal offers and retention campaigns, but not all customers are equally valuable or equally likely to respond. This project simulates a real analyst workflow: taking raw customer data, cleaning it, building out business KPIs, applying advanced SQL techniques, segmenting customers by value, and packaging the results into a dashboard a marketing or retention team could actually use.

The analysis is structured as a progression — starting with exploration and cleaning, moving through business reporting and advanced SQL, and ending with segmentation and BI-ready outputs.

## 🗂️ Dataset

| | |
|---|---|
| **Source** | [IBM Watson Analytics – Marketing Customer Value Data](https://www.kaggle.com/datasets/pankajjsh06/ibm-watson-marketing-customer-value-data) (Kaggle) |
| **Size** | ~9,134 rows × 24 columns |
| **Grain** | One row per customer policy |
| **License** | CC BY-NC-SA 4.0 — non-commercial use |

Raw CSV is not included in this repo. Download it directly from the Kaggle link above to reproduce the analysis.

## 🛠️ Tech Stack

- **SQL** (PostgreSQL) — exploration, cleaning, analysis, advanced querying
- **Power BI** — dashboarding and stakeholder-facing reporting

## 📁 Repository Structure

```
├── sql/
│   ├── 01_Data_Exploration.sql
│   ├── 02_Data_Cleaning.sql
│   ├── 03_Business_Analysis.sql
│   ├── 04_Window_Functions.sql
│   ├── 05_CTEs.sql
│   ├── 06_Customer_Segmentation.sql
│   ├── 07_Advanced_Insights.sql
│   └── 08_PowerBI_KPIs.sql
├── dashboard/
│   ├── insurance_dashboard.pdf
│   └── interactive demo gif 
├── insights/
│   └── clv_insight_pdf_report
└── README.md
```

## 🔍 What Each SQL File Covers

| File | Focus |
|---|---|
| `01_Data_Exploration.sql` | Row counts, distinct values, distributions, first-pass data quality checks |
| `02_Data_Cleaning.sql` | Date formatting, null handling, type corrections, category standardization |
| `03_Business_Analysis.sql` | Core KPIs — CLV by segment, response rate by offer/channel, claims patterns |
| `04_Window_Functions.sql` | `RANK`, `DENSE_RANK`, `ROW_NUMBER`, `LAG`, `LEAD`, `NTILE` for ranking and comparison |
| `05_CTEs.sql` | Multi-step, layered analysis using common table expressions |
| `06_Customer_Segmentation.sql` | `CASE`-based segmentation — CLV quartiles, value tiers, risk grouping |
| `07_Advanced_Insights.sql` | Executive-level, cross-dimensional business questions |
| `08_PowerBI_KPIs.sql` | Final aggregated queries structured to feed the dashboard |

## 📊 Dashboard

An interactive Power BI dashboard translates the SQL analysis into a stakeholder-facing view — including CLV and response rate KPIs, segment breakdowns, and channel/offer performance.

📷 *Screenshots available in* `BI DASHBOARD/pdf/`

## 💡 Insights


- **💰 $73.1M** total Customer Lifetime Value across 9,134 policyholders, against **$851K** in monthly premium revenue and **$3.96M** in total claims.

- **⚠️ 22% of customers are overinsured** — 2,003 customers pay above-average premiums ($100+/mo) while carrying below-average CLV (under $10,000). This is the single largest structural risk in the portfolio.

- **🚗 Vehicle class is the strongest CLV predictor** — Luxury SUV and Luxury Car owners carry ~2.5x the average CLV of standard sedan owners ($17,123 vs. $6,632), but also file ~3.2x larger claims ($1,130 vs. $352).

- **📞 The Agent sales channel converts at nearly 2x every other channel** — 19.15% response rate vs. 10.9–11.8% for Web, Branch, and Call Center combined.

- **🏆 Special Auto is the smallest policy segment (4.1%) but the highest-value one** — average CLV of $8,594, ahead of Personal Auto ($8,027) and Corporate Auto.

- **💎 Premium coverage remains the most profitable tier** despite filing the largest claims per customer — average profit of $10,244/customer vs. $6,812 for Basic coverage, meaning pricing already outpaces risk.

- **🌎 Geography and income are weak CLV predictors** — CLV varies by only 2.7% across states and 5.7% across income quartiles, meaning policy structure and vehicle choice matter far more than *who* the customer is or *where* they live.

- **🎯 54 high-CLV customers (>$40,000) have not responded** to the current marketing campaign — a small, high-value, immediately actionable target list for a follow-up campaign.

- **📊 Overall campaign response rate is a modest 14.32%**, and responders are not meaningfully higher-value than non-responders — the current campaign isn't yet preferentially reaching high-CLV customers.

## ▶️ How to Reproduce

1. Download the dataset from Kaggle and load it into PostgreSQL (or your SQL engine of choice)
2. Run the SQL scripts in order, `01` through `08`
3. Open `dashboard/insurance_dashboard.pbix` in Power BI Desktop to explore the dashboard

## 👤 About Me

ESHA SOHAIL — Data Analyst

