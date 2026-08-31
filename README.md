# 🏬 Fictional Stores: Retail Sales & Customer Analytics Dashboard

An interactive Power BI report built to analyze retail performance across a multi-country grocery chain — covering revenue, profit, returns, and customer retention, with dynamic metric switching and year-over-year trending.

## 2. Short Description / Purpose

The Fictional Stores Dashboard is a Power BI report designed to help business users explore sales and profitability across **24 stores in the USA, Canada, and Mexico** from **1997–1998**. It combines transaction, returns, product, and customer data into a single star-schema model, letting stakeholders pivot between Revenue and Profit views on demand and track performance trends, customer retention, and return rates over time. Its intended users are mid level execs, regional managers, stores managers who seek to understand trends and characteristics of stores and products globally. 

## 3. Tech Stack

The dashboard was built using the following tools and technologies:

- **Power BI Desktop** – Main data visualization platform used for report creation.
- **Power BI Service** - Connected the dataflow from BI service workspace and published it to web(public).
- **Power Query** – Data transformation and cleaning layer for reshaping and preparing the source tables.
- **DAX (Data Analysis Expressions)** – Powers 27 measures, including time-intelligence calculations (YoY and MoM comparisons via `DATEADD`), customer retention/cohort logic, and dynamic titles.
- **Field Parameters** – A `Metric Selection` parameter lets users toggle visuals between Revenue and Profit without duplicating charts.
- **Data Modeling** – A star schema with one fact table (Transactions Data) and a returns fact table, related to five lookup/dimension tables (Customers, Products, Stores, Regions, Calendar) via nine relationships.

## 4. Data Source

The data is clean dataset picked up from Maven analytics. Imported the data files to OneDrive folder and created a dataflow in Power BI Service using the files and used that dataflow to create the dashboard in Power BI desktop.  

## 5. Features / Highlights

**Business Problem**
Retail leadership needs a fast way to answer questions like: Which products and stores drive the most profit? How is revenue trending year-over-year? Are customers being retained, and where are returns eating into margin? Raw transactional data makes these questions slow to answer.

**Goal of the Dashboard**
To deliver an interactive tool that:
- Lets users switch seamlessly between Revenue and Profit as the primary metric across visuals.
- Surfaces trends, YoY/MoM growth, and anomalies without manual pivoting.
- Tracks customer retention and return rates alongside sales performance.
- Uncovers trends sales/products revenue trends of stores and products across regions and countries.

**Walkthrough of Key Visuals**
- **Metric Toggle (Field Parameter)** — A single control (`Metric Selection`) swaps the underlying measure (Revenue vs. Profit) across trend charts and titles, which update dynamically to reflect the active selection.
- **Exec Summary Page** — Includes a trending chart with a conditionally-formatted, dynamic title, plus a Top 5 Products visual that re-ranks based on the selected metric.
- **Customers Page** — Includes a donut chart (also metric-aware via dynamic title) alongside customer-focused KPIs: Total Customers, Retained Customers, and Customer Retention %.
- **YoY & MoM Trend Measures** — Previous Year/Previous Month comparisons for Revenue and Profit, plus growth-percentage measures, support trend and variance analysis.
- **Returns Analysis** — Quantity Returned, Return Rate, and Previous Month Returns quantify how returns affect net performance.
- **Weekday/Weekend Split** — Transaction counts broken out by weekend vs. weekday to reveal shopping-pattern differences.

**Business Impact & Insights**
- **Performance Monitoring:** Leadership can track Revenue and Profit trends month-over-month and year-over-year from one view.
- **Product Strategy:** The metric-aware Top 5 Products visual highlights which products to prioritize under either a revenue or profitability lens.
- **Customer Loyalty:** Retention measures identify how much of the customer base is being kept year-over-year, informing loyalty and marketing investment.
- **Margin Protection:** Return Rate and returns-related measures flag where returned inventory is eroding profit.


