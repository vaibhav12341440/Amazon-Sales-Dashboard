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

 
