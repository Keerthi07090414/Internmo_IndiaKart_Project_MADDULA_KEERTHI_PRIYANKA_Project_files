# IndiaKart E-Commerce Analytics Project

**Name:** MADDULA KEERTHI PRIYANKA
**Internship:** Internmo Virtual Internship (Data Analyst)
**Project:** IndiaKart E-Commerce Analytics
**Data period:** 24-Jun-2023 to 23-Jun-2025

End-to-end analysis of IndiaKart e-commerce data: 8 tables and 222,200 rows (customers, orders, order_items, products, payments, returns, inventory, suppliers). The project covers data cleaning, exploratory analysis, 10 business KPIs, a 5-page Power BI dashboard and a management report for the CEO.

## Project phases

| Phase | Description | Status |
|---|---|---|
| 1 | Data cleaning and quality check | Done |
| 2 | Exploratory data analysis (10 charts) | Done |
| 3 | 10 business KPIs, plus bonus cohort analysis | Done |
| 4 | Power BI dashboard (5 pages) and management report | Done |

## Repository contents

**Phase 1: Data cleaning**
- `Phase1_DataCleaning_MADDULA_KEERTHI_PRIYANKA.ipynb` and `.pdf`: profiling, missing values, duplicates, data types, outliers, referential integrity and the Data Quality Report

**Phase 2: Exploratory data analysis**
- `Phase2_EDA_MADDULA_KEERTHI_PRIYANKA.ipynb` and `.pdf`: 10 charts, each with an observation, and key takeaways
- `01_monthly_orders.png` to `10_aov_segment.png`: the 10 charts

**Phase 3: Business KPIs**
- `Phase3_KPIs_MADDULA_KEERTHI_PRIYANKA.ipynb` and `.pdf`: 10 KPIs, a KPI summary table and the cohort analysis
- `11_cohort_retention.png`: cohort retention heatmap

**Phase 4: Dashboard and report**
- `Phase4_Dashboard_MADDULA_KEERTHI_PRIYANKA.pbix` and `.pdf`: 5-page Power BI dashboard (Revenue Overview, Category Performance, Customer Insights, Operations, Inventory Alert)
- `Phase4_Report_MADDULA_KEERTHI_PRIYANKA.pdf`: 3-page management summary report for the CEO

## KPI scorecard

| # | KPI | Result | Target | Status |
|---|---|---|---|---|
| 1 | Total order value (GMV) | Rs. 314.74 crore | - | - |
| 2 | Net revenue (delivered orders) | Rs. 205.39 crore (65.3% of GMV) | - | - |
| 3 | Average order value | Rs. 63,198 | - | - |
| 4 | Cancellation rate | 12.0% | below 10% | Not met |
| 5 | Return rate | 13.3% of delivered orders (30.8% by the brief's formula) | below 8% | Not met |
| 6 | Premium vs Regular customer value | 1.47x | 3x | Not met |
| 7 | Average monthly GMV growth (full months) | +0.51% | - | - |
| 8 | Top category share (Electronics) | 57.7% | below 60% | Met (close) |
| 9 | Payment failure rate | 3.50% | below 2% | Not met |
| 10 | Inventory fill rate | 92.2% | above 95% | Not met |

## Key findings

- **Failed payments drive cancellations.** All 1,748 failed payments ended in cancelled orders (Rs. 10.74 crore), which is 29.2% of all cancellations. Without them the cancellation rate would be about 8.5%.
- **Only 65% of order value becomes delivered revenue.** Sales are flat at about Rs. 13 crore a month, and full-month sales are 1.2% lower than a year earlier. There is no visible Diwali (Oct-Nov) spike.
- **Revenue is concentrated.** Electronics earns 57.7% of delivered revenue and the top three categories earn about 83%. Uttar Pradesh and Maharashtra give about 35% of all orders.
- **Premium customers order more often, not more per order.** They average about 8.6 orders against 5.7 for Regular customers, but their average order value is no higher than other segments.
- **Returns are mostly quality and delivery issues.** About 56% of returns are damaged, wrong, defective, not-as-described or poor-quality items.
- **Stock is below target.** 78 products (7.8%) are below their reorder level, and Hyderabad-WH4 (89.2%) and Bengaluru-WH3 (90.1%) are the weakest warehouses.
- **Retention is flat.** About 18% of each registration cohort orders in any month from Month 2 to Month 6, with no visible drop-off.

## Data quality notes

- No duplicate rows or keys, and all table relationships are valid.
- 10,071 orders (20.1%) have no line items, including 6,584 delivered orders worth Rs. 18.97 crore, so category figures cover about 91% of net revenue.
- 20.5% of orders are dated before the customer's registration date, so the cohort analysis counts only orders on or after registration.
- 1,740 return records are attached to orders that were cancelled or not yet delivered.
- The first and last months (Jun 2023 and Jun 2025) are partial months and are excluded from growth comparisons.

## Tools

Python, pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook, Power BI Desktop

## Note

The raw CSV files, data dictionary and SQL schema are provided by Internmo and are not included in this repository.
