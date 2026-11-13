# IndiaKart E-Commerce Analytics: Phase 1 (Data Cleaning & Quality Check)

**Name:** MADDULA KEERTHI PRIYANKA
**Internship:** Internmo Virtual Internship (Data Analyst)
**Project:** IndiaKart E-Commerce Analytics
**Data period:** 24-Jun-2023 to 23-Jun-2025

## About this phase

Phase 1 covers loading and profiling 8 tables (222,200 rows in total), checking missing values, duplicates, data types, outliers and referential integrity, converting date columns to datetime, and writing a Data Quality Report.

## Tables analysed

customers, orders, order_items, products, payments, returns, inventory, suppliers

## What was checked

- Missing values in every column of every table
- Duplicate rows and duplicate primary keys
- Data types, with all date columns converted from text (DD-MM-YYYY) to datetime
- Outliers in final_amount, plus negative amounts, invalid quantities and ages
- Referential integrity across 7 table relationships (0 orphan records)
- Business checks: delivery date before order date, payment failure rate, returns without a matching order, out-of-stock products, customers with zero orders

## Key findings

- No duplicate rows or duplicate primary keys in any table
- All 7 foreign key relationships are valid
- Only 2 columns have missing values: orders.delivered_date (17,501 rows, 35%) and payments.refund_date (100%)
- Payment failure rate is 3.50%, above the 2% target
- 312 orders (0.62%) are above Rs. 5 lakh, with a maximum of about Rs. 11.33 lakh
- final_amount is right-skewed (mean Rs. 62,948 vs median Rs. 24,183)
- 457 customers have zero orders and 2 products are out of stock

## Tools

Python, pandas, NumPy, Jupyter Notebook

## Files

- `Phase1_DataCleaning_MADDULA_KEERTHI_PRIYANKA.ipynb`: the full notebook with code, outputs and the Data Quality Report

## Note

The raw CSV files are provided by Internmo and are not included in this repository.
