# Olist Brazilian E-Commerce Sales Analytics

An end-to-end sales analytics project built to simulate a real Sales Analyst / Business Analyst workflow — from raw data to an interactive business dashboard.

## Project Overview
This project analyzes 100,000+ real orders from Olist, a major Brazilian e-commerce marketplace, covering sales, sellers, products, payments, delivery performance, and customer reviews across 2016-2018. The goal was to build a complete pipeline — cleaning and structuring raw data in Python, modeling and querying it in PostgreSQL, and presenting insights through an interactive Power BI report.

## Dataset
**Brazilian E-Commerce Public Dataset by Olist** (Kaggle)
🔗 https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

9 relational CSV files covering orders, order items, payments, reviews, products, customers, sellers, and geolocation data.

## Tools & Tech Stack
- **Python** (Pandas, Google Colab) — data cleaning, translation, feature engineering
- **PostgreSQL** (pgAdmin) — relational database, SQL analysis queries
- **Power BI** — data modeling, DAX measures, interactive dashboard

## Pipeline

### 1. Python — Data Cleaning
- Loaded and inspected 9 raw CSV files
- Handled missing values (delivery dates, review comments, product categories)
- Translated product categories from Portuguese to English
- Converted date columns, created derived fields
- Exported cleaned tables for database loading

📂 [`/python/Sales_Data_Cleaning.ipynb`](./python/Sales_Data_Cleaning.ipynb)

### 2. SQL — Data Modeling & Analysis
- Loaded cleaned data into PostgreSQL as 7 related tables with proper foreign keys
- Wrote analysis queries covering:
  - Revenue by product category and by state
  - Top sellers by revenue
  - Monthly sales trends
  - Delivery delay analysis by state
  - Review score vs delivery performance
  - Payment method breakdown

📂 [`/sql/queries.sql`](./sql/queries.sql)

### 3. Power BI — Dashboard
A 3-page interactive report connected live to the PostgreSQL database:

- **Page 1 — Overview:** Total Revenue, Total Orders, Avg Review Score, Avg Delivery Delay KPIs; Monthly Revenue Trend; Top 10 Product Categories; Top 10 States by Revenue
- **Page 2 — Product & Seller Performance:** Top 10 Sellers by Revenue; Category Performance (Revenue vs Volume); Volume vs Revenue scatter plot; interactive slicers
- **Page 3 — Delivery & Customer Satisfaction:** Avg Delivery Delay by State; Review Score comparison (Late vs On-Time deliveries); Delivery Delay Trend over time

📂<img width="1208" height="683" alt="image" src="https://github.com/user-attachments/assets/ced34664-0d19-44db-b13c-0619a06bae02" />


## Key Insights
- Revenue grew steadily from early 2017, peaking in late 2017/early 2018
- São Paulo (SP) drives the largest share of revenue by a wide margin
- Health & Beauty and Watches/Gifts are the top-performing product categories
- ~7.9% of orders are delivered late — and late deliveries correlate with a noticeably lower average review score (~2.5 vs ~4.1)
- Delivery performance improved significantly over time, from an average 35-day delay in 2016 to under 15 days by 2018

## Author
**Deep Sarkar**
Data Analyst | SQL, Python, Power BI, Tableau
