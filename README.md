# Superstore Sales Performance Analysis

## Project Overview
This project analyses 4 years of retail sales data (2023–2026) from a US-based superstore to uncover what is driving revenue and profit — and what is hurting it. The analysis covers regional performance, product profitability, customer behaviour, and the impact of discounting on profit margins.

**Tools used:** Microsoft Excel · SQL (SQLite) · Tableau

---

## Business Questions Answered
- Which regions and product categories are the most profitable?
- Which sub-categories are consistently losing money?
- Who are the top customers by revenue?
- Do higher discounts lead to lower profit?
- Are there seasonal patterns in monthly sales?

---

## Dataset
- **Source:** Sample Superstore Dataset
- **Size:** 10,194 rows · 21 columns
- **Period:** January 2023 – December 2026
- **Fields:** Orders, customers, products, regions, sales, profit, discounts, shipping

---

## Tools & Process

### Excel — Data Cleaning & Exploration
- Checked for duplicates, nulls, and inconsistent category names
- Created two calculated columns:
  - `Profit Margin %` = Profit / Sales
  - `Revenue per Order` = Sales × Quantity
- Built 3 pivot tables: Sales by Region, Top 10 Sub-Categories by Profit, Monthly Sales Trend
- Built an interactive dashboard with KPI cards and charts

### SQL (SQLite) — Querying & Analysis
- Imported cleaned data into SQLite via DB Browser
- Wrote 9 queries progressing from basic aggregations to CTEs and window functions
- Key techniques used: `GROUP BY`, `HAVING`, `CASE WHEN`, `NTILE()`, `LAG()`, CTEs

### Tableau — Visualisation & Dashboard
- Connected directly to the Excel data source
- Built 4 visualisations: regional bar chart, sub-category profit chart, monthly trend line, discount vs profit scatter plot
- Published interactive dashboard to Tableau Public

---

## Key Findings

### 1. West region leads in both sales and profit
The West generated $739,814 in sales and $110,799 in profit — the highest of all four regions. Central had the weakest profit margin despite ranking third in sales, suggesting inefficient discounting or higher costs in that region.

### 2. Three sub-categories are losing money
Tables, Bookcases, and Supplies all generated negative profit across the full 4-year period. These sit within the Furniture category, which also carries the highest average discount rate (17%).

### 3. Discounts above 20% destroy profit
Analysis of discount brackets showed a clear pattern — average profit turns negative once discounts exceed 20%. Orders with no discount had the highest average profit. This suggests the current discounting strategy needs to be reviewed and capped.

### 4. Copiers are the most profitable sub-category
Copiers generated $56,094 in profit — nearly $11,000 more than Phones in second place. Technology as a category has the lowest average discount (13%) and the highest total profit ($146,543).

### 5. Sales spike every Q4
Consistent revenue spikes appear every November and December across all four years, confirming strong seasonal demand. This pattern can be used to plan inventory and marketing spend in advance.

### 6. Top customer: Sean Miller at $25,043 revenue
The top 20% of customers (by revenue) account for a disproportionate share of total sales — a classic 80/20 pattern that suggests loyalty and retention efforts should focus on this tier.

---

## Recommendations
- **Cap discounts at 20%** — anything above this consistently generates losses
- **Review Furniture pricing strategy** — Tables and Bookcases need margin improvement or should be deprioritised
- **Double down on Technology** — highest profit, lowest discounts, strong sub-category performance
- **Invest in Q4 readiness** — stock up and run targeted campaigns ahead of November each year
- **Build a top-customer retention programme** — the top 20% of customers drive outsized revenue

---

## Files in This Repository
| File | Description |
|---|---|
| `sample_superstore.xlsx` | Cleaned Excel file with pivot tables and dashboard |
| `superstore_queries.sql` | All 9 SQL queries with comments |

## Tableau Dashboard
🔗 [View Live Dashboard](https://public.tableau.com/app/profile/tess.kamau/viz/SuperstoreSalesAnalysis_17765991673530/SuperstoreSalesDashboard)

---

## Author
**Tess Kamau**
- wanjirutee4@gmail.com
- [LinkedIn](https://linkedin.com/in/tesskamau-a23708354)
- [GitHub](https://github.com/Tee-ai63)
