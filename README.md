# UK-based-E-commerce-sales-transaction
Analysis data of UK-based E-commerce sales transaction

## Project Overview

This project analyzes one year of transactional data from a UK-based e-commerce business using Power BI, Python, and DAX. The goal of the project is to transform raw sales transactions into actionable business insights through data modeling, customer segmentation, product analysis, seasonality analysis, and cancellation behavior analysis.

The dashboard was designed to simulate a real business intelligence workflow used by data analysts and BI teams.

---

# Project Goals

The main objectives of this project were:

* Analyze overall business performance
* Identify top-performing products
* Understand customer purchasing behavior
* Detect seasonal sales patterns
* Analyze cancellation trends and operational risks
* Build an interactive executive-style dashboard
* Practice real-world data modeling and DAX development

---

# Thought Process

Instead of building visuals immediately, the project was approached using a business-first analytical workflow.

The process started with understanding the dataset structure and identifying key business questions:

* Is the business growing?
* Which products drive the most revenue?
* Which customers are most valuable?
* Are sales seasonal?
* Which countries contribute the most?
* Are cancellations concentrated in certain products or customers?

From there, the dashboard structure was designed around analytical themes rather than random charts.

The project evolved from simple revenue reporting into deeper operational and behavioral analysis.

Key analytical decisions included:

* Separating Product and Customer dimension tables from the transaction table
* Excluding cancelled orders from completed sales calculations
* Using percentage contribution metrics instead of only raw values
* Creating customer segmentation using sales value and transaction frequency
* Building a dedicated cancellation analysis page to identify operational risks

---

# Data Preparation

## Source Dataset

* UK-based E-Commerce Transaction Dataset
* One year of transactional sales data

## Data Cleaning & Transformation

Performed using Python and Power BI:

* Removed missing customer records where necessary
* Identified cancelled invoices using invoice prefixes
* Created calculated transaction values
* Built reusable customer and product dimension tables

---

# Data Modeling

The project follows a simplified star schema structure:

* Fact Table:

  * SalesTransaction

* Dimension Tables:

  * Product
  * Customer
  * Calendar

Relationships were configured to improve filtering behavior, scalability, and DAX calculations.

---

# Customer Table Creation (Python)

Python was used to aggregate customer-level metrics from raw transactional data, including:

* CustomerCompletedSales
* CustomerTransactionCount
* CustomerCancelCount
* CustomerBuyValue
* CustomerBuyUnits
* Country

This allowed cleaner segmentation and customer analysis inside Power BI.

---

# Key DAX Measures

Examples of measures developed during the project:

## Sales Metrics

* _NetSales
* _TotalInvoices
* _TotalQuantitySold
* _AveragePrice

## Product Metrics

* _ProductSalesValue
* _ProductUnitsSold
* _ProductContributionPct

## Customer Metrics

* _MedianCustomerSales
* CustomerSegment
* Customer Count

## Cancel Metrics

* _CancelledInvoices
* _CancelledQuantity
* _CancelledValue
* _CancelRate

---

# Customer Segmentation Logic

Customers were segmented using spending behavior and transaction frequency.

Segments included:

* VIC (Very Important Customer)
* High-Value Occasional
* Loyal Customers
* Low Engagement

This segmentation helped identify customer value distribution and engagement patterns.

---

# Dashboard Structure

## 1. Executive Overview

<p align="center">
  <img src="Power%20BI%20PNG/UK-based%20E-commerce%201.png" width="1000">
</p>

* KPI cards
* Monthly sales trends
* Country performance
* Product contribution analysis

## 2. Product Performance

<p align="center">
  <img src="Power%20BI%20PNG/UK-based%20E-commerce%202.png" width="1000">
</p>

* Product sales analysis
* Units sold trends
* Product contribution %
* Product concentration insights

## 3. Geography & Seasonality

<p align="center">
  <img src="Power%20BI%20PNG/UK-based%20E-commerce%203.png" width="1000">
</p>

* Revenue by country
* Seasonal sales trends
* Q4 growth analysis

## 4. Customer Insights

<p align="center">
  <img src="Power%20BI%20PNG/UK-based%20E-commerce%204.png" width="1000">
</p>

* Customer segmentation
* Customer distribution by segment
* Customer purchasing behavior

## 5. Cancel Analysis

<p align="center">
  <img src="Power%20BI%20PNG/UK-based%20E-commerce%205.png" width="1000">
</p>

* Cancel rate by product
* Cancel rate by country
* Customer cancellation behavior
* Operational risk analysis

---

# Tools & Technologies

## Power BI

* Dashboard design
* Data modeling
* Interactive visualizations
* DAX calculations

## Python

* Data preparation
* Dimension table creation
* Aggregation logic

## DAX

* CALCULATE
* SUMX
* DIVIDE
* FILTER
* MEDIANX
* ALL / REMOVEFILTERS

---

# Key Insights

Some notable findings from the analysis:

* Strong revenue growth occurred during Q4
* A small number of products contributed heavily to yearly sales
* Some products showed highly seasonal demand patterns
* Revenue concentration existed across a limited number of countries
* Cancellation behavior varied significantly by product and customer type
* Customer segmentation revealed distinct high-value and low-engagement groups

---

# Skills Demonstrated

## Technical Skills

* Power BI
* DAX
* Python (Pandas)
* Data Modeling
* Dashboard Design
* Business Intelligence

## Analytical Skills

* Customer Segmentation
* Revenue Analysis
* Seasonality Analysis
* Operational Risk Analysis
* KPI Development
* Data Storytelling

---

# Future Improvements

Potential future enhancements include:

* RFM customer segmentation
* Predictive sales forecasting
* Churn analysis
* Customer lifetime value modeling
* Advanced drill-through reporting
* SQL database integration

---

# Conclusion

This project helped strengthen both technical and analytical skills by simulating a real-world business intelligence workflow from raw data preparation to executive dashboard reporting.

The final dashboard focuses not only on revenue reporting, but also on customer behavior, operational performance, and strategic business insights.
