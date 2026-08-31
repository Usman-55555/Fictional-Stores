# Fictional Stores — Retail Analytics Power BI Project

A multi-page Power BI dashboard analyzing revenue, profit, store performance, and customer behavior for a fictional multi-country grocery/retail chain operating in the USA, Canada, and Mexico.

## Overview

Built on a star-schema dataset covering transactions from **1997–1998**, across **24 stores**, **~1,559 products**, and **~9,600 customers**, this project demonstrates end-to-end BI development: data modeling, DAX measure design, dynamic report interactivity, and business insight generation.

## Report Pages

- **Executive Dashboard** — high-level KPIs with a field-parameter-driven Top 5 Products chart (toggle between Revenue and Profit), and a geographic breakdown by country.
- **Store Performance** — store-type and regional performance, including a KPI visual with a trend-axis area chart.
- **Product Details** — matrix breakdown of Revenue, Profit, and YOY growth by product, filterable by country and year.

## Data Model

Star schema with:
- **Fact tables:** `Transactions Data`, `Returns_Data`
- **Dimension tables:** `Calendar_Lookup`, `Customers_Lookup`, `Products_Lookup`, `Stores_Lookup`, `Regions_Lookup`
- **Field parameter:** `Metric Selection` (Total revenue / Profit)

Full schema, relationships, and calculated-column documentation: see [`Fictional_Stores_Project_Documentation.docx`](./Fictional_Stores_Project_Documentation.docx).

## Key DAX Techniques

- Year-over-year and month-over-month time intelligence using `DATEADD`
- Cohort-based customer retention (`INTERSECT` of current vs. prior-year customer sets)
- Field-parameter-driven dynamic Top N filtering
- A `HASONEVALUE`-guarded time-intelligence pattern to prevent misleading YOY results under multi-period filter selections

## Key Insights

| Question | Finding |
|---|---|
| Overall YOY revenue growth (1997→1998) | **+112.18%** — driven mostly by Canada/Mexico market launches |
| USA-only YOY revenue growth | **+8.40%** — the more accurate organic-growth figure |
| Customer retention (1997→1998) | **85.99%** of 1997 customers returned in 1998 |
| Weekend share of transactions | **28.40%** of all transactions |
| Declining products despite overall growth | Several SKUs (e.g. National Egg Substitute) fell **34–37%** YOY in the USA |

## Tech Stack

`Power BI Desktop` · `DAX` · `Power Query (M)` · `Star schema modeling`

## Files

- `Fictional_Stores_Project_Documentation.docx` — full project documentation (data model, Power Query notes, DAX reference, insights, recommendations, resume/interview writeup)
- `Fictional Stores.pbix` — the Power BI report file

## Notes

This is a portfolio/practice project built on a fictional dataset — figures and business context are illustrative, not real company data.
