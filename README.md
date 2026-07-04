# Online Retail II — Exploratory Data Analysis (Week 1)

## Project Overview
This project is Week 1 of the AI/ML Internship at **ITSimplera Solutions**. The goal is to explore a real e-commerce transaction dataset and produce a full Exploratory Data Analysis (EDA) that helps a retail business understand its customers, top products, and revenue by country — ahead of building a future recommendation system.

The analysis is **observation-only**: no rows are removed, filtered, or corrected. Every data quality issue found (missing values, cancellations, outliers) is reported rather than cleaned, so decisions on how to treat them can be made deliberately later.

## Dataset Information
- **Name:** Online Retail II
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
- **Rows:** 525,461
- **Columns:** InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country
- **Coverage:** UK-based online retailer, 2009–2011

## Environment Setup
```bash
git clone https://github.com/MUQADAS-03/online-retail-eda-week1.git
cd online-retail-eda-week1
pip install -r requirements.txt
jupyter notebook week_1.ipynb
```

## Feature Engineering Steps
- `Revenue` = Quantity × UnitPrice
- `InvoiceMonth` = month extracted from InvoiceDate
- `IsCancelled` = flag for invoices starting with "C"
- `DayOfWeek`, `Hour` = extracted from InvoiceDate for demand-pattern analysis
- RFM (Recency, Frequency, Monetary) fields per customer

## EDA Findings
- UK accounts for **85.9%** of total revenue
- **20.54%** of rows have no CustomerID
- **1.94%** of invoices are cancellations
- Revenue peaks in **November** (£1,422,654.64)
- **71.1%** of identified customers are repeat buyers
- Outliers make up 6.7%–11% of rows, likely wholesale/B2B orders

## Author
**Muqadas Yasin** — AI/ML Internship, ITSimplera Solutions
