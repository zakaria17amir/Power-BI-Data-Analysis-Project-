# DAX Calculations for Sales Analysis

This document contains essential DAX calculations used for analyzing sales data in Power BI.

## **1️⃣ Yearly Profit Margin**
Calculates the profit margin for the year by dividing total Gross Revenue by total Net Revenue.

```DAX
Yearly Profit Margin = 
DIVIDE(
    SUM('Sales in USD'[Gross Revenue USD]), 
    SUM('Sales in USD'[Net Revenue USD]), 
    0  // To avoid division by zero errors
)
```

## **2️⃣ Year-to-Date (YTD) Profit**
Aggregates net revenue from the start of the year to the current date.

```DAX
YTD Profit = 
TOTALYTD(
    SUM('Sales in USD'[Net Revenue USD]),  // Aggregating Net Revenue USD
    'Calendar'[Date]  // Using Calendar Table's Date Column
)
```

## **3️⃣ Median Sales**
Finds the median (middle value) of Gross Revenue.

```DAX
Median Sales = 
MEDIAN('Sales in USD'[Gross Revenue USD])
```

## **4️⃣ Quarterly Profit**
### **Using TOTALQTD** (Automatically calculates quarter-to-date profit)

```DAX
Quarterly Profit = 
TOTALQTD(
    SUM('Sales in USD'[Net Revenue USD]),  // Aggregates Net Revenue
    'Calendar'[Date]  // Uses the Calendar Table's Date Column
)
```

### **Using DATESQTD** (Alternative way to calculate quarter-to-date profit)

```DAX
Quarterly Profit = 
CALCULATE(
    SUM('Sales in USD'[Net Revenue USD]), 
    DATESQTD('Calendar'[Date])
)
```

## **📌 Notes**
- Ensure that a **Calendar Table** is present and related to the `Sales in USD` table.
- The `DIVIDE` function prevents division by zero errors.
- `TOTALYTD` and `TOTALQTD` dynamically calculate cumulative values up to the current period.
- The **Median Sales** measure is useful for statistical analysis of sales data.

## **📂 Usage**
- Add these measures to Power BI visuals such as **Cards, Tables, and Charts**.
- Use the **Performance Analyzer** to ensure DAX calculations run efficiently.


