Power BI Data Analysis and Dashboard Development
Project Overview
This project involved transforming raw Excel data into a fully interactive Power BI dashboard by performing data cleaning, modeling, visualization, and automation. The goal was to provide actionable insights for business decision-making through structured reporting and optimized performance.

Project Workflow
1. Data Preparation and Cleaning
Imported raw Excel files containing Sales, Purchases, Exchange Rates, and Country Data.
Performed data cleaning by:
Removing duplicates.
Handling missing values.
Standardizing column names.
Adding relevant calculated columns for deeper insights.
2. Configuring Data Sources in Power BI
Connected the cleaned data to Power BI Service.
Configured automatic data refresh to ensure up-to-date insights.
3. Data Modeling and Relationships
A robust data model was designed with structured table relationships:

Key Relationships:
Countries ↔ Exchange Data on Exchange ID (1:1)
Sales ↔ Countries on Country ID (Many-to-One)
Purchases ↔ Sales on Order ID (1:1)
Calendar Table ↔ Purchases on Purchase Date (Many-to-One)
Sales in USD (calculated table) ↔ Sales on Order ID (Many-to-One)
Key Data Enhancements:
Created a Calendar Table using DAX for time-based analysis.
Developed Sales in USD table to convert local currency sales into USD.
4. DAX Aggregations and Measures
To improve data analysis, the following DAX measures were created:

Yearly Profit Margin: Gross Revenue / Net Revenue.
Quarterly Profit: Aggregated using DATESQTD.
Year-to-Date (YTD) Profit: Computed using TOTALYTD.
Median Sales: Calculated using the MEDIAN function.
5. Sales Report Development
A Sales Report was created featuring key visualizations:

📊 Loyalty Points by Country – Bar Chart
📈 Quantity Sold by Product – Column Chart
🥧 Median Sales Distribution by Country – Pie Chart
📉 Median Sales Over Time – Line Chart
🔢 Sum of Stock – Card Visual
📦 Sum of Quantity Purchased – Card Visual
💰 Median Sales – Card Visual
6. Profit Report Development
A Profit Report was created to track financial performance:

📊 Net Revenue by Product – Bar Chart
🥯 Yearly Profit Margin by Country – Donut Chart
📉 Yearly Profit Margin Over Time – Area Chart
📈 YTD Profit – Card Visual
💰 Sum of Net Revenue (USD) – Card Visual
📊 Sum of Gross Revenue (USD) – KPI
7. Publishing Reports and Creating Dashboards
Published the Sales and Profit Reports to Power BI Web Service.
Created interactive dashboards for both Web and Mobile versions.
Designed an optimized layout for mobile users to ensure accessibility.
8. Adding Alerts and Subscriptions
To enhance automation and user engagement, the following features were implemented:

Configured Alerts:

Set up notifications for specific KPIs exceeding thresholds.
Alerts triggered based on monthly sales, profit margins, and stock levels.
Set Up Monthly Email Subscriptions:

Scheduled automated email reports for Sales and Profit Reports.
Ensured business users received key insights directly via email.
9. Performance Optimization
Used Performance Analyzer to optimize DAX queries.
Ensured report load times were below 200ms for efficiency.
Removed unnecessary visuals for improved performance and responsiveness.
Project Outcome
End-to-End Data Analysis Pipeline from raw data to actionable insights.
Powerful interactive dashboards providing real-time insights.
Automated reports and alerts, ensuring timely decision-making.
Optimized performance with fast query execution and seamless user experience.
This project delivered a highly effective Power BI solution that improved data visualization, reporting automation, and business intelligence.