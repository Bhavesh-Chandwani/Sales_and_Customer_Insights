# 📊 Sales & Customer Insights Analysis using SQL

Leveraging 30+ advanced SQL queries to uncover customer behavior, revenue drivers, geographical dependencies, and strategic business opportunities from transactional sales data.

## Executive Summary

Modern retail businesses generate enormous volumes of transactional data, yet making strategic decisions requires converting that data into meaningful business intelligence.

This project analyzes customer, product, and sales data to uncover the key drivers of revenue and identify areas of operational risk.

The analysis revealed several critical business challenges:

- **96.46% of revenue is generated from a single product category (Bikes)**, creating significant revenue concentration risk.
- **Approximately 40% of customers originate from the United States**, indicating heavy dependence on one geographic market.
- **VIP customer conversion remains low**, limiting customer lifetime value.
- **Sales performance fluctuates considerably over time**, suggesting seasonal demand and inconsistent revenue generation.

Using **30+ advanced SQL queries**, this project converts raw transactional data into actionable business insights and strategic recommendations that support      data-driven decision making.

---

## Problem Statement

The business dataset shows extreme revenue concentration in one product category and one geography, combined with inconsistent temporal performance and low VIP / repeat-customer conversion — creating a high revenue-risk profile. The analytical goal is to quantify concentration and retention shortfalls, diagnose drivers (product mix, seasonality, customer segments), and recommend measurable interventions to increase revenue per customer, diversify revenue sources, and improve retention.

---

## Objective

The objective of this project is to quantify these risks, identify the underlying business drivers, and provide actionable recommendations using advanced SQL analysis.

---

## Business Questions Answered

This project answers several business-critical questions, including:

1. Which product categories contribute the highest revenue?
2. Which products generate the highest and lowest sales?
3. Which countries contribute the most customers and revenue?
4. How dependent is the business on the US market?
5. What is the customer distribution across Regular, New, and VIP segments?
6. Which customers generate the highest lifetime revenue?
7. How does revenue change over months and years?
8. Is revenue concentrated among a few product categories?
9. What seasonal sales patterns exist?
10. What strategies can improve customer retention and revenue diversification?

---

## Dataset Overview

| Dataset | Description |
|---------|-------------|
| Customer | Customer Identity, Customer Demographics and Location Information |
| Product | Product ID, Number, Name, Categories, Subcategories, Cost, Date |
| Sales Fact | Order Number, Product Key, Customer Key, Order Date, Shipping Date, Due Date, Sales Amount, Quantity, Price |

---

# Tech Stack

| Category | Technologies |
|----------|--------------|
| Language | SQL |
| SQL Concepts | CTEs, Views, Subqueries |
| Advanced SQL | Window Function, Ranking and Running Totals|
| Analysis| Aggregation, Joins, Time-Series Analysis, Segmentation |
| Queries Written | 30+ Advanced SQL Queries |

---

# Database Architecture

            +----------------------+
            |      Customer        |
            |----------------------|
            | CustomerKey (PK)     |
            | CustomerId           |
            | CustomerNumber       |
            | FirstName            |
            | LastName             |
            | Country              |
            | MaritalStatus        |
            | Gender               |
            | BrithDate            |
            | CreateDate           |
            +----------+-----------+
                       |
                       | CustomerKey (FK)
                       |
                       ▼
        +----------------------------------+
        |         Sales Fact Table         |
        |----------------------------------|
        | OrderNumber (PK)                 |
        | CustomerKey (FK)                 |
        | ProductKey (FK)                  |
        | OrderDate                        |
        | ShippingDate                     |
        | DueDate                          |
        | SalesAmount                      |
        | Quantity                         |
        | Price                            |
        +----------------+-----------------+
                         ▲
                         |
                         | ProductKey (FK)
                         |
            +------------+-------------+
            |          Product         |
            |--------------------------|
            | ProductKey (PK)          |
            | ProductId                |
            | ProductNumber            |
            | ProductName              |
            | CategoryId               |
            | Category                 |
            | Subcategory              |
            | Maintenance              |
            | Cost                     |
            | ProductLine              |
            | Startdate                |
            | Price                    |
            +--------------------------+

---

# SQL Analysis Outputs

### Revenue By Product Category

<a href="03_Result_Set_Images/12 Total Revenue Generated for Each Category.png">
    <img src="03_Result_Set_Images/12 Total Revenue Generated for Each Category.png">
</a>

---

## Customer Segmentation

<a href="03_Result_Set_Images/24. Customer Segmentation.png">
    <img src="03_Result_Set_Images/24. Customer Segmentation.png">
</a>

---

### Total Customers By Countries

<a href="03_Result_Set_Images/08. Total Customers By Countries.png">
    <img src="03_Result_Set_Images/08. Total Customers By Countries.png">
</a>

---

### Total Sales Per Month and Running Sales Overtime

<a href="03_Result_Set_Images/21. Total Sales Per Month and Running Total Over Time.png">
    <img src="03_Result_Set_Images/21. Total Sales Per Month and Running Total Over Time.png">
</a>

---

### Top 5 Produts in terms of Revenue

<a href="03_Result_Set_Images/15. Top 5 Products in terms of Revenue.png">
    <img src="03_Result_Set_Images/15. Top 5 Products in terms of Revenue.png">
</a>

---

### Top 5 Worst Performing Products

<a href="03_Result_Set_Images/16. Top 5 Worst Performing Products.png">
    <img src="03_Result_Set_Images/16. Top 5 Worst Performing Products.png">
</a>

---

### Product Segmentation Analysis

<a href="03_Result_Set_Images/23. Product Segmentation Analysis.png">
    <img src="03_Result_Set_Images/23. Product Segmentation Analysis.png">
</a>

---

### Contribution of Categories to Overall Sales

<a href="03_Result_Set_Images/25. Contribution of Categories to Overall Sales.png">
    <img src="03_Result_Set_Images/25. Contribution of Categories to Overall Sales.png">
</a>

---

# Key Analytical Insights

## 1. Revenue & Category Concentration

### Findings

- **96.46% of total revenue comes from Bikes**
- Accessories and Clothing contribute less than **5%**
- Mountain Bikes dominate overall sales

### Business Risk

The business is heavily dependent on one product category, making revenue highly vulnerable to changes in bike demand, pricing, or competition.

### Recommendation

- Introduce **Bike + Accessories bundles**
- Cross-sell safety equipment and apparel
- Increase accessory contribution from **<5% to 20%+**

---

## 2. Geographic Dependency

### Findings

- The **United States contributes nearly 40%** of customers and revenue.
- Other regions such as Canada, France, and Germany show comparatively lower engagement.

### Business Risk

Revenue is highly concentrated in a single geographic market, increasing exposure to regional economic fluctuations.

### Recommendation

- Expand localized marketing campaigns
- Strengthen European market penetration
- Develop region-specific promotional strategies

---

## 3. Customer Lifecycle & VIP Conversion

### Customer Segmentation

| Segment | Customers |
|----------|----------:|
| Regular | 14,839 |
| New | 1,990 |
| VIP | 1,655 |

### Findings

Although customer acquisition is healthy, only a small percentage transition into high-value (VIP) customers.

### Recommendation

- Loyalty and rewards programs
- Personalized product recommendations
- Automated email marketing campaigns
- Repeat purchase incentives

---

## 4. Seasonality & Sales Trends

### Findings

- Significant revenue spike observed during **2013**
- Noticeable decline in later periods
- Monthly sales fluctuate considerably

### Business Insight

Sales exhibit seasonal patterns rather than consistent long-term growth.

### Recommendation

- Identify peak demand periods
- Launch promotional campaigns before seasonal peaks
- Improve inventory planning using historical trends

---

# Product Performance Analysis

### Top Performers

- Mountain Bike product line dominates revenue generation.
- High-ticket products generate the majority of overall sales.

### Underperformers

Products such as:

- Socks
- Patches
- Small Accessories

contribute very little revenue individually.

### Recommendation

- Bundle low-performing products
- Eliminate consistently underperforming inventory
- Promote accessories alongside bike purchases

---

# Customer Revenue Analysis

### Findings

- Highest customer revenue is approximately **13K**
- Revenue distribution is relatively balanced
- No dominant enterprise-level customers

### Business Insight

The business relies on a broad customer base rather than a few high-value accounts.

### Recommendation

Increase Customer Lifetime Value (CLV) through:

- Membership programs
- Subscription services
- Personalized promotions
- Repeat purchase campaigns

---

# Strategic Business Recommendations

| Business Challenge | Recommended Strategy |
|-------------------|----------------------|
| Revenue concentrated in Bikes | Expand Accessories & Clothing through cross-selling |
| Low VIP conversion | Launch loyalty and retention programs |
| Geographic dependency | Expand marketing beyond the US |
| Seasonal fluctuations | Forecast demand and run seasonal campaigns |
| Weak accessory sales | Bundle products and optimize merchandising |
| Product imbalance | Diversify product portfolio across price segments |

---

# SQL Technical Highlights

### This project demonstrates practical SQL techniques commonly used in business analytics.

- Advanced SQL Concepts
- Common Table Expressions (CTEs)
- Nested Subqueries
- Views for Report Creation
- Window Functions
- Ranking Functions
- Running Totals
- Aggregate Functions
- Multi-table Joins
- CASE Expressions
- Date Functions
- Customer Segmentation
- Revenue Analysis
- Time-Series Analysis

### Total SQL Queries: 30+

----

# Repository Structure

```text
sales-insights-analysis/
├── 01_Datasets/
├── 02_Scripts/
├── 03_Result_Set_Images/
├── End to End Sales & Customer Intelligence Anal...
├── LICENSE
└── README.md
```

---

# 📦 Project Deliverables

This repository contains the complete analytical workflow—from raw SQL queries to executive-level business recommendations.

| Deliverable | Description |
|-------------|-------------|
| 🗄️ **SQL Scripts** | 30+ advanced SQL queries utilizing CTEs, Subqueries, Views, Window Functions, Joins, and Aggregations to solve real-world business problems. |
| 📊 **Business Presentation** | Executive-style PowerPoint presentation summarizing key findings, business insights, and strategic recommendations. |
| 🖼️ **SQL Query Outputs** | Screenshots of SQL query result sets demonstrating the analytical process and supporting business conclusions. |
| 📄 **Project Documentation** | Comprehensive README explaining the business problem, analytical methodology, insights, recommendations, and repository structure. |

---

# Final Outcome

This project demonstrates how advanced SQL can be applied to solve real-world business problems by transforming transactional data into actionable insights. Through analytical techniques such as customer segmentation, revenue concentration analysis, time-series evaluation, and product performance assessment, the project delivers data-driven recommendations that support strategic decision-making and business growth.

---

## 📬 Connect With Me

<div align="center">

| Platform | Link |
|----------|------|
| 💼 LinkedIn | [Let's Connect](https://www.linkedin.com/in/bhavesh-chandwani) |
| 📧 Gmail | [bhavesh101714@gmail.com](mailto:bhavesh101714@gmail.com) |

</div>

---

# 👨‍💻 Author

### Bhavesh Chandwani


---

⭐ If you found this useful, feel free to connect and discuss data-driven strategies!
