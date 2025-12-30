# 📊 ElectroHub – Sales Data Analysis using Power BI
*(Covers Data Modeling, DAX & Advanced Visual Analytics)*

### Dashboard Link : https://app.powerbi.com/links/eLJ9RQR5tk?ctid=bc5b2879-3fac-469a-b8c4-994705bc09d7&pbi_source=linkShare

## Project Overview

**ElectroHub** is a retail sales analytics project developed using **Power BI** to analyze sales, profit, quantity sold, discounts, promotions, and customer behavior.  
The project demonstrates a complete **end-to-end Business Intelligence workflow**, from data cleaning and modeling to building interactive dashboards.

This project highlights strong skills in:
- Data Modeling & Star Schema Design  
- Power Query (ETL & Data Cleaning)  
- DAX Measures  
- KPI Design  
- Interactive Dashboard Development  

---

## Business Context

ElectroHub operates across multiple product categories:

- Electronics  
- Footwear  
- Clothing  
- Home Appliances  
- Accessories  
- Kitchenware  
- Bags  
- Personal Care  

The goal of this analysis is to:
- Identify top and underperforming products  
- Analyze sales and profit trends  
- Evaluate promotion effectiveness  
- Compare performance across time periods  
- Enable data-driven decision-making  

---

## Data Model Overview

A **Star Schema** was implemented for clarity and performance.

### Fact Table
**Fact_Sales**
- Order ID  
- Date  
- Customer ID  
- Product ID  
- Promotion ID  
- Units Sold  
- Price Per Unit  
- Discount  
- Discount Percentage  
- Net Sales  
- Profit  
- Total Sales  

### Dimension Tables

**Dim_Customers**
- Customer ID  
- Customer Name  
- City  
- State  
- Email  
- Phone Number  
- Pincode  

**Dim_Product**
- Product ID  
- Product Name  
- Product Line  
- Price Per Unit (INR)  

**Dim_Promotion**
- Promotion ID  
- Promotion Name  
- Ad Type  
- Coupon Code  
- Price Reduction Type  

**Date Table**
- Date  
- Month  
- Quarter  
- Year  

---

## Data Cleaning & Transformation (Power Query)

The following data preparation steps were performed:

- Standardized data types across all tables  
- Removed null and invalid values  
- Created conditional columns (Discount Percentage by Promotion)  
- Merged:
  - Product dimension with Fact table  
  - Customer dimension with Fact table  
  - Promotion dimension with Fact table  
- Ensured referential integrity  
- Renamed columns for readability  
- Validated row consistency after merges  

---

## Business Requirements Covered

The Power BI report answers the following business questions:

1. **Top & Bottom 5 Products** by:
   - Sales  
   - Profit  
   - Quantity Sold  

2. **Sales Trends Over Time**
   - Daily  
   - Monthly  
   - Quarterly  
   - Yearly  

3. **Relationship Between Sales & Profit**
   -Correlation analysis using scatter plots  

4. **Period Comparison Analysis**
   -Compare Sales, Profit & Quantity between two user-selected periods  

5. **Average Discount by Promotion Category**
   -Evaluate promotion effectiveness  

6. **Total Number of Orders**
   -High-level KPI  

7. **Detailed Order-Level Analysis**
   - Sales, Profit, Discount, Net Sales  
   - Filterable by:
     - Product  
     - Date  
     - Customer  
     - Promotion  

8. **Sales by City**
   -Geographic sales distribution  

---

## Dashboard Pages

### 🔹 Page 1: Sales Overview & Trends
- Total Orders KPI  
- Sales by City (Map)  
- Monthly Sales Trend  
- Profit vs Net Sales (Scatter Chart)  
- Average Discount by Promotion  

**Focus:** Overall business performance  

### 🔹 Page 2: Product Performance Analysis
- Top 5 Products by Sales / Profit / Quantity  
- Bottom 5 Products by Sales / Profit / Quantity  

**Focus:** Product-level insights  

### 🔹 Page 3: Period Comparison Analysis
- Dual date slicers  
- Side-by-side comparison:
  - Total Sales  
  - Total Profit  
  - Total Quantity Sold  

**Focus:** Time-based performance evaluation  

### 🔹 Page 4: Edit Interactions
- Controlled visual interactions  
- Improved cross-filter behavior 
 **Focus:** Improve user experience by controlling visual interactions and avoiding unnecessary cross-filtering.


### 🔹 Page 5: Detailed Table View
- Order-level transaction data  
- Fully interactive filtering  

**Focus:** Granular inspection & validation  

---

## Key DAX Measures (Examples)

```DAX
Total Sales = SUM(Fact_Sales[Total Sales])

Total Profit = SUM(Fact_Sales[Profit])

Total Quantity Sold = SUM(Fact_Sales[Units Sold])

Number of Orders = DISTINCTCOUNT(Fact_Sales[Order ID])

Average Discount =
AVERAGE(Fact_Sales[Discount Percentage])
```
## Key Insights

- A small group of products contributes a major share of overall revenue, indicating a classic Pareto (80/20) effect.
- Higher discounts do not always lead to higher profits, highlighting the importance of balanced pricing and promotion strategies.
- A strong positive correlation exists between sales and profit, confirming that increased sales volumes generally drive profitability.
- Sales data shows clear seasonal patterns, with certain months consistently outperforming others.
- The **Electronics** category dominates overall sales contribution across products and regions.

---

## Deployment

- Data modeled and validated using **Power BI Desktop**.
- Interactive dashboards designed for deployment on **Power BI Service**.
- Optimized data model and visuals to ensure scalability and performance.

---

## Skills Demonstrated

- Power BI Desktop & Power BI Service  
- Data Modeling using Star Schema  
- Power Query (ETL & Data Cleaning)  
- DAX Calculations & Measures  
- KPI Design and Visualization  
- Sales & Retail Analytics  
- Interactive and User-Driven Dashboard Design  

---

## Conclusion

The **ElectroHub Sales Data Analysis** project demonstrates a complete real-world Business Intelligence solution, starting from raw data cleaning and transformation and ending with insight-driven, interactive dashboards.  
It showcases strong analytical thinking, data modeling expertise, and visualization skills, making it highly relevant for **Data Analyst, Business Analyst, and BI Developer** roles.

