# Amazon-Sales-Dashboard
## Project Objective 
The objective of this project is to analyze and visualize Amazon sales data using Power BI to provide actionable insights for business decision-making. This dashboard aims to help stakeholders track key metrics, identify trends, and optimize sales strategies.

## Dataset Used
- <a href="https://github.com/vaibhav12341440/Amazon-Sales-Dashboard/blob/main/global_superstore.xlsx">Amazon sales dashboard
## Questions(KPIs)
✅ Total Sales Revenue – Overall revenue generated from all sales.
✅ Total Units Sold – Number of products sold in a given period.
✅ Best-Selling Products – Top products by revenue and quantity sold.
✅ Category-Wise Sales – Performance analysis of different product categories.
✅ Stock Turnover Rate – How frequently inventory is sold and replaced.
✅ Return Rate – Percentage of sold products returned by customers.✅ Sales Growth Rate – Percentage increase/decrease in sales over time.
✅ Order Processing Time – Average time to process an order.
✅ Shipping Time – Average time from order placement to delivery.
✅ Order Fulfillment Rate – Percentage of successfully completed orders.
✅ Cost Per Order – Total operational cost divided by the number of orders.

Dashboard : <a herf="https://github.com/vaibhav12341440/Amazon-Sales-Dashboard/blob/main/AmazonDashboard.pbix">

Dashboard image :<a href="https://github.com/vaibhav12341440/Amazon-Sales-Dashboard/blob/main/Screenshot%202025-03-31%20151548.png">

## Process 


---

### **🔹 Step 1: Data Collection**  
📌 Gather sales data from sources like:  
- Amazon Seller Central Reports  
- Excel/CSV files  
- Databases (SQL Server, MySQL, etc.)  
- API integration (if needed)  

---

### **🔹 Step 2: Data Cleaning & Preparation**  
📌 Use **Power Query (ETL Process)** to:  
✅ Remove duplicates & null values  
✅ Convert data types (e.g., dates, numbers)  
✅ Create calculated columns (Profit, Total Sales, etc.)  
✅ Format date fields for time-based analysis  

---

### **🔹 Step 3: Data Modeling**  
📌 **Create relationships** between tables (Fact & Dimension Model):  
- **Fact Table:** Sales Transactions (Order details, Revenue, Profit)  
- **Dimension Tables:** Products, Customers, Regions, Date Table  

🔹 **Example Relationship Model:**  
- **Sales Table** (Order ID, Product ID, Customer ID, Date)  
- **Products Table** (Product ID, Name, Category, Price)  
- **Customers Table** (Customer ID, Name, Location)  
- **Date Table** (Date, Month, Year)  

---

### **🔹 Step 4: Create Key Performance Indicators (KPIs)**  
📌 Use **DAX (Data Analysis Expressions)** for calculated measures:  

✅ **Total Sales Revenue:**  
```DAX
Total Sales = SUM(Sales[Revenue])
```

✅ **Total Profit:**  
```DAX
Total Profit = SUM(Sales[Profit])
```

✅ **Profit Margin:**  
```DAX
Profit Margin = DIVIDE([Total Profit], [Total Sales]) * 100
```

✅ **Average Order Value (AOV):**  
```DAX
AOV = DIVIDE([Total Sales], DISTINCTCOUNT(Sales[Order ID]))
```

✅ **Sales Growth Rate:**  
```DAX
Sales Growth = ([Total Sales] - CALCULATE([Total Sales], PREVIOUSMONTH(Date[Date]))) / CALCULATE([Total Sales], PREVIOUSMONTH(Date[Date]))
```

---

### **🔹 Step 5: Create Interactive Visualizations**  
📌 **Choose appropriate visuals:**  
✅ **KPI Cards** – Display **Total Sales, Total Orders, Profit Margin**  
✅ **Bar Charts** – Top-selling products & sales by category  
✅ **Line Charts** – Monthly & yearly **sales trends**  
✅ **Map Visuals** – Sales distribution across regions  
✅ **Donut Charts** – Customer segmentation & purchase behavior  
✅ **Tables & Filters** – Allow users to drill down into specific data  

---

### **🔹 Step 6: Dashboard Customization & Formatting**  
📌 **Improve user experience** by:  
✅ Applying **themes & color schemes** for readability  
✅ Adding **filters & slicers** (Date Range, Product Category, Region)  
✅ Using **tooltips & drill-through options** for deeper insights  

---

### **🔹 Step 7: Testing & Optimization**  
📌 **Verify dashboard performance & accuracy:**  
✅ Check for **calculation errors in DAX formulas**  
✅ Optimize **large datasets** by reducing unnecessary columns  
✅ Test **interactivity (filters, slicers, drill-throughs)**  

---

### **🔹 Step 8: Publishing & Sharing**  
📌 **Deploy the dashboard** to **Power BI Service**  
✅ Share with team members via **Power BI Workspace**  
✅ Schedule **automated data refresh** for real-time updates  
✅ Set up **row-level security (RLS)** for data access control  

---

## Dashboard

![Screenshot 2025-03-31 151548](https://github.com/user-attachments/assets/18a5e31d-b366-429e-98b5-9cd61642ac36)

## Project Insight
### **Project Insight & Final Conclusion of the Dashboard**  

This dashboard provides a **comprehensive overview of Amazon's global sales performance** across different years, focusing on sales, profitability, product performance, and regional distribution. Below are the **key insights** and the **final conclusion** of the data presented.  

---

### **📊 Project Insights**  

#### 1. Overall Sales Performance
- **Total Sales:** ₹12.64 million  
- **Total Product Units Sold:** 3,788  
- **Key Performance Indicator (KPI):** 178K  
- **Returns:** 1,464 (which may indicate areas for product/service improvement)  

#### 2. Sales Distribution 
- **By Segment:**  
  - **Consumer (51.48%)** leads sales.  
  - **Corporate (30.25%)** comes next.  
  - **Home Office (18.27%)** contributes the least.  

- **By Market:**  
  - **USCA (31.98%)** and **Europe (26%)** generate the most revenue.  
  - **Asia Pacific (18.7%)**, **LATAM (17.12%)**, and **Africa (6.2%)** show lower contributions.  

- **Sales by Region (Map View):**  
  - **Hotspots:** Europe, Africa, and South America.  
  - **Underperforming regions:** Africa and parts of Asia.  

#### 3. Profitability Insights  
- **Top 5 Profitable Products:**  
  - **Canon Imaging (₹25K)** and **Cisco Smart (₹17K)** are the highest-earning products.  
  - **Motorola, Hoover, and Sauder** also perform well.  

- **Bottom 5 Products (Losses):**  
  - **Cubify Cube (-₹8.9K)** is the biggest loss-making product.  
  - **Lexmark and Motorola** also contribute to negative profits.  

- **Top Customers by Profit:**  
  - **Tamara Chand, Ray Buch, and Sanjit Chand** generate the highest profits.  

---

## **✅ Final Conclusion**  
1. **Strongest Performing Segment & Market:**  
   - **Consumer segment** dominates sales, meaning B2C (Business-to-Consumer) is more profitable than Corporate or Home Office.  
   - **USCA and Europe** are the biggest revenue-generating markets, so efforts should focus on expanding and optimizing sales there.  

2. **Areas of Improvement:**  
   - **Africa and parts of Asia** are **underperforming markets** and need better marketing or localized strategies.  
   - **Certain products (Cubify Cube, Lexmark, etc.) are making losses**, indicating a need for a **product discontinuation or optimization strategy**.  

3. **Opportunities for Growth:**  
   - **Best-selling products like Canon, Cisco, and Motorola should be expanded further** to maximize profit.  
   - **Returning customer engagement (Top customers list)** indicates that **customer retention is key** for high profits.  


