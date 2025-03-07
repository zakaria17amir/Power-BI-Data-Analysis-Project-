# **Power BI Data Analysis Project**

## **📌 Overview**
This project focuses on **data cleaning, modeling, visualization, and reporting** using **Power BI**. The dataset includes **sales, purchases, exchange rates, and country data**, transformed into an **interactive dashboard**. Key insights include **profit analysis, sales performance, and financial metrics**.

The final output consists of:
- **Sales Report**: Tracks sales performance, quantity sold, and stock levels.
- **Profit Report**: Analyzes net revenue, profit margins, and key financial indicators.
- **Power BI Dashboard**: Interactive web and mobile dashboards with automated alerts and subscriptions.

---

## **📊 Features**
✅ **Data Cleaning & Preparation**: Processed raw Excel files for accurate reporting.  
✅ **Data Modeling**: Structured **table relationships** and implemented **bi-directional filtering**.  
✅ **DAX Calculations**: Created **custom measures** for profit analysis, YTD, and median sales.  
✅ **Interactive Visualizations**: Developed **Sales & Profit Reports** with dynamic visuals.  
✅ **Performance Optimization**: Used **Performance Analyzer** to optimize query speed.  
✅ **Automation**: Configured **alerts and email subscriptions** for key business metrics.  

---

## **📁 Project Structure**
📂 PowerBI-Project
 ├── 📂 Data
 │    ├── raw_sales_data.xlsx            # Original sales data
 │    ├── cleaned_data.xlsx              # Cleaned and processed data
 ├── 📂 Reports
 │    ├── sales_report.pbix              # Power BI Sales Report
 │    ├── profit_report.pbix             # Power BI Profit Report
 ├── 📂 Screenshots
 │    ├── sales_dashboard.png            # Sales Dashboard Preview
 │    ├── profit_dashboard.png           # Profit Dashboard Preview
 ├── 📂 Documentation
 │    ├── project_description.md         # Detailed project documentation
 │    ├── data_model_diagram.png         # ER Diagram of data model
 │    ├── dax_calculations.md            # List of all DAX formulas used
 ├── README.md                            # Project overview and usage guide



---

## **🛠 Data Processing & Modeling**
### **🔹 Data Cleaning**
- Removed **duplicates and null values**.
- Standardized column names for consistency.
- Added **relevant calculated columns**.

### **🔹 Data Model Relationships**
| Table 1  | Table 2  | Relationship | Type |
|----------|---------|-------------|------|
| **Countries** | Exchange Data | `Exchange ID` | `1:1` |
| **Sales** | Countries | `Country ID` | `Many:1` |
| **Purchases** | Sales | `Order ID` | `1:1` |
| **Calendar Table** | Purchases | `Date` | `Many:1` |
| **Sales in USD** | Sales | `Order ID` | `Many:1` |

### **🔹 DAX Calculations**
- **Yearly Profit Margin** → `Gross Revenue / Net Revenue`
- **Quarterly Profit** → `DATESQTD` function for time-based aggregation
- **YTD Profit** → `TOTALYTD` for cumulative year-to-date profit
- **Median Sales** → `MEDIAN()` function for central sales performance

---

## **📊 Reports & Dashboards**
### **1️⃣ Sales Report**
- **Loyalty Points by Country** – Bar Chart  
- **Quantity Sold by Product** – Column Chart  
- **Median Sales Distribution by Country** – Pie Chart  
- **Median Sales Over Time** – Line Chart  
- **Sum of Stock** – Card Visual  
- **Sum of Quantity Purchased** – Card Visual  
- **Median Sales** – Card Visual  

### **2️⃣ Profit Report**
- **Net Revenue by Product** – Bar Chart  
- **Yearly Profit Margin by Country** – Donut Chart  
- **Yearly Profit Margin Over Time** – Area Chart  
- **YTD Profit** – Card Visual  
- **Sum of Net Revenue (USD)** – Card Visual  
- **Sum of Gross Revenue (USD)** – KPI  

---

## **🚀 How to Use**
### **1️⃣ Open the Project in Power BI**
1. Download the `*.pbix` files from the `Reports` folder.
2. Open them in **Power BI Desktop**.
3. Refresh the data to ensure the latest updates.

### **2️⃣ Publish to Power BI Service**
1. Click **Publish** to upload reports to **Power BI Web Service**.
2. Create **Dashboards** for both **Web & Mobile versions**.
3. Configure **scheduled refresh** for real-time updates.

### **3️⃣ Configure Alerts & Subscriptions**
- Set **threshold alerts** for important metrics (e.g., low stock, revenue drops).
- Schedule **monthly report subscriptions** to receive email updates.

---

## **⚡ Performance Optimization**
✅ Used **Performance Analyzer** to evaluate query execution times.  
✅ Ensured **DAX queries execute in under 200ms** for efficiency.  
✅ Reduced unnecessary visuals to **optimize report load time**.  

---

## **📩 Contact & Contribution**
Feel free to **contribute** or raise issues!  
If you have suggestions or need modifications, reach out via **GitHub Issues**. 🚀

---

## **🌟 Future Improvements**
- Integrate **Real-Time Streaming Data** for live updates.  
- Add **AI-powered predictive analytics** using **Azure ML** in Power BI.  
- Implement **role-based access** for better security.  

