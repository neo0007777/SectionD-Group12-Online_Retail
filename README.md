🛒 Global Retail Transaction Analysis & Customer Segmentation
1️⃣ Project Overview

This project analyzes transactional data from an international e-commerce retailer to uncover:

High-value customers (RFM Analysis)

Sales trends by country and time

Return/refund patterns

Product performance insights

Customer segmentation opportunities

The objective is to transform messy raw data into actionable business insights that support better marketing, inventory, and revenue strategies.

2️⃣ Dataset Details

Dataset Name: Online Retail II
Source: UCI Machine Learning Repository / Kaggle
Sector: Retail (E-commerce)
Rows (Original): ~500,000+
Rows (Sample Used): 10,000–15,000 (for Google Sheets performance)
Columns: 8

Column Name	Description
InvoiceNo	Unique transaction ID
StockCode	Product code
Description	Product name
Quantity	Number of items purchased
InvoiceDate	Date & time of transaction
UnitPrice	Price per item
CustomerID	Unique customer ID
Country	Country of purchase
3️⃣ File Details
File Name	Description
raw_retail_sample.csv	Cleaned subset of original dataset
Master_Google_Sheet	Contains Raw Data, Cleaned Data, Pivot Tables
Dashboard	Visual analytics summary
Returns_Analysis	Analysis of cancelled orders
RFM_Sheet	Customer segmentation sheet
4️⃣ Data Dictionary
🔎 Column Issues & Cleaning Log
Column	Issue Found	Action Taken	Reason
CustomerID	~20% missing	Labeled as "Guest_User"	Preserve transaction data
Quantity	Negative values	Separated into Returns sheet	Identify cancellations
InvoiceNo	Some start with “C”	Tagged as Cancelled	Business logic
StockCode	POST, PADS, M etc.	Removed	Not actual products
InvoiceDate	Text format	Converted to DateTime	Enable time analysis
5️⃣ Data Cleaning Notes

✔ Filtered cancelled transactions (InvoiceNo starting with “C”)
✔ Created separate Returns table
✔ Removed non-product stock codes
✔ Converted InvoiceDate to proper date format
✔ Standardized Country names
✔ Created new column: Total Revenue = Quantity × UnitPrice

6️⃣ Dataset Analysis (Include Screenshots Here)

📸 Insert screenshots of:

Raw Data (before cleaning)

Cleaned Data sheet

Pivot table example

Dashboard charts

7️⃣ Key Insights & Statistics
📊 Sales Insights

Top Revenue Country: United Kingdom

Most Sold Product Category: Home & Decorative Items

Peak Sales Month: November–December (Holiday Season)

🔄 Returns Analysis

Return rate ≈ X% of total transactions

Certain countries show higher refund frequency

Some SKUs have significantly high return ratios

👤 Customer Insights (RFM)

Top 10% customers contribute ~60% revenue

High Recency + High Frequency = Loyal Segment

Identified 3 major customer clusters:

VIP Customers

Regular Buyers

At-Risk Customers

8️⃣ Dashboard Summary

Dashboard includes:

Sales by Country (Map/Bar Chart)

Monthly Revenue Trend (Line Chart)

Top 10 Products (Bar Chart)

Customer Segmentation Pie Chart

Return Rate KPI

9️⃣ Advanced Analysis (Bonus Section)
✅ RFM Analysis

Recency: Days since last purchase

Frequency: Number of transactions

Monetary: Total spend

Customers grouped into segments using RFM score ranking.

✅ Cohort Analysis

Grouped customers by first purchase month

Measured retention over time

✅ Market Basket (Optional)

Identified frequently co-purchased items

🔮 Forecasting (Optional Bonus)

Used monthly revenue trends to project:

Expected Q1 sales growth

Seasonal spikes prediction

Can be done using:

Moving average

Linear trend line

Google Sheets FORECAST() function

💡 Business Recommendations

Target VIP customers with loyalty rewards

Investigate high-return SKUs

Launch country-specific promotions

Bundle frequently purchased products

Retarget “At-Risk” customers with email campaigns
