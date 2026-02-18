
# 🛒 Global Retail Transaction Analysis & Customer Segmentation

## 📌 Project Overview

This project analyzes transactional data from a global e-commerce retailer to uncover key revenue drivers, customer behavior patterns, and operational insights. The goal is to transform raw transactional data into actionable business intelligence using data cleaning, exploratory analysis, and dashboard visualization.

The project focuses on identifying high-value customers, understanding sales trends, analyzing product performance, and detecting return patterns to support strategic decision-making.

---

## 🎯 Objectives

* Analyze total revenue, sales volume, and return rate
* Identify top-performing products and revenue contributors
* Understand customer purchasing behavior and segmentation
* Detect peak sales hours and seasonal trends
* Analyze return and cancellation patterns
* Build an interactive dashboard for business insights

---

## 📊 Dataset Information

**Dataset Name:** Online Retail II

**Source:** UCI Machine Learning Repository / Kaggle

**Industry:** E-commerce / Retail

### Dataset Size

| Metric        | Value                       |
| ------------- | --------------------------- |
| Original Rows | 500,000+                    |
| Sample Used   | 10,000–15,000              |
| Columns       | 8                           |
| Countries     | Multiple (Global customers) |
| Time Period   | 2009–2011                  |

---

## 📁 Dataset Schema

| Column      | Description                   |
| ----------- | ----------------------------- |
| InvoiceNo   | Unique transaction identifier |
| StockCode   | Product code                  |
| Description | Product name                  |
| Quantity    | Number of items purchased     |
| InvoiceDate | Date and time of purchase     |
| UnitPrice   | Price per item                |
| CustomerID  | Unique customer identifier    |
| Country     | Customer location             |

---

## 🧹 Data Cleaning & Preprocessing

Several preprocessing steps were performed to ensure data quality and analytical accuracy:

### Data Cleaning Actions

* Removed invalid stock codes (POST, PADS, etc.)
* Converted InvoiceDate into proper DateTime format
* Created new calculated column:

  **TotalRevenue = Quantity × UnitPrice**
* Separated return transactions (negative quantity)
* Identified cancelled invoices (InvoiceNo starting with "C")
* Handled missing CustomerID values by labeling as "Guest_User"
* Standardized country names and formats

---

## 📈 Key Performance Indicators (KPIs)

Based on analysis and dashboard results:

| KPI                 | Value          |
| ------------------- | -------------- |
| Total Revenue       | £203,729.90   |
| Total Items Sold    | 122,855        |
| Total Return Value  | £8,636.56     |
| Return Rate         | 3.08%          |
| Top Revenue Country | United Kingdom |

These metrics are also visualized in the dashboard KPI section.

---

## 📊 Dashboard Features

The interactive dashboard includes:

### Revenue Analysis

* Monthly revenue trend
* Revenue by hour of day
* Revenue by country

### Product Analysis

* Top 10 best-selling products
* Product revenue contribution

### Customer Analysis

* Customer segmentation (Guest vs Registered users)
* High-value customer identification

### Returns Analysis

* Return rate calculation
* Return value tracking
* Cancellation identification

---

## 🔍 Key Insights

### Revenue Insights

* Total revenue generated: £203,729.90
* United Kingdom contributes the majority of total revenue
* Sales peak between **11 AM and 3 PM**
* Strong seasonal performance during holiday months

### Customer Insights

* Registered customers contribute the majority of revenue
* A small percentage of customers generate a large portion of total sales
* Customer segmentation reveals VIP, Regular, and At-Risk customers

### Product Insights

* Home and decorative items dominate sales
* Top products contribute disproportionately to revenue
* Product-level analysis helps identify high-performing SKUs

### Returns Insights

* Overall return rate is low (3.08%)
* Negative quantity transactions indicate returns or cancellations
* Some products have higher return frequency

---

## 👤 Customer Segmentation (RFM Analysis)

Customer segmentation was performed using the RFM model:

* **Recency:** Days since last purchase
* **Frequency:** Number of transactions
* **Monetary:** Total revenue generated

Customer segments identified:

* VIP Customers
* Regular Customers
* At-Risk Customers
* Guest Users

This segmentation enables targeted marketing strategies.

---

## 🛠 Tools & Technologies Used

* Google Sheets
* Pivot Tables
* Data Cleaning Techniques
* Data Visualization
* RFM Customer Segmentation
* Business Intelligence Dashboarding

---

## 💼 Business Impact & Recommendations

Based on analysis, the following strategies are recommended:

### Customer Strategy

* Target VIP customers with loyalty programs
* Retarget at-risk customers with promotions
* Encourage guest users to register

### Product Strategy

* Promote top-performing products
* Investigate high-return products
* Bundle frequently purchased items

### Marketing Strategy

* Focus campaigns during peak sales hours
* Launch country-specific promotions
* Use customer segmentation for personalized marketing

---

## 🚀 Future Improvements

* Implement predictive revenue forecasting
* Perform cohort analysis for customer retention
* Apply market basket analysis for cross-selling
* Build automated dashboard using Power BI or Python
* Integrate real-time data pipelines

---

## 📊 Conclusion

This project demonstrates the complete data analytics workflow:

* Raw data cleaning
* Exploratory analysis
* Customer segmentation
* Dashboard creation
* Business insight generation

The analysis enables data-driven decision-making for improving revenue, customer retention, and operational efficiency.
