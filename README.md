# DSA3050A Mid-Semester Practical Examination

- Paul mbuvi Mwende
- 669984

## Dataset Information
- **Dataset:** Sample - Superstore Sales Dataset
- **Source URL:** https://www.kaggle.com/datasets/vivek468/superstore-dataset-final
- **Number of Rows:** 9,994
- **Number of Columns:** 21

## Business Problem
As a Business Intelligence Analyst for a retail organization, 
the goal is to analyze sales performance, profitability, and 
regional trends to support data-driven decision-making across 
product categories and customer segments.

## Power Query Transformations Performed

### A. Basic Data Cleaning
1. Renamed unclear columns (Row ID, Ship Mode, Sub-Category, Postal Code)
2. Changed data types (Order Date, Ship Date → Date; Sales, Profit → Decimal)
3. Removed duplicate records using Row_ID
4. Removed blank rows
5. Trimmed and cleaned text columns (Customer Name, City, State, Region, Category)
6. Replaced inconsistent values in Shipping_Mode column
7. Removed unnecessary columns (Country, Row_ID)

### B. Intermediate Transformations
1. Split Order ID column into Order_Region_Code, Order_Year, Order_Number
2. Merged City and State into City_State column
3. Created custom column: Revenue_After_Discount = Sales * (1 - Discount)
4. Created conditional column: Profit_Status (Profitable / Loss)
5. Extracted Year, Month, Quarter, Day from Order Date
6. Filtered rows: Profit_Status = Profitable AND Sales > 10
7. Sorted data by Sales descending
8. Added Index column starting from 1

### C. Advanced Power Query Tasks
1. Extracted text before delimiter from Customer ID column
2. Used Column Profiling to identify data quality issues
3. Created Group By summary (Sales_Summary) with Total_Sales, Total_Profit, Order_Count
4. Created Date Table in Power Query (2014-2017)
5. Created Reference Query (Technology_Sales) filtered to Technology category

## Dashboard Visuals Created
1. KPI Card — Total Sales
2. KPI Card — Total Profit
3. KPI Card — Total Quantity
4. Bar Chart — Sum of Sales by Category
5. Column Chart — Sum of Profit by Region
6. Line Chart — Sum of Sales by Year (with drill-down)
7. Donut Chart — Sum of Sales by Segment
8. Table Visual — Order details with Profit Status
9. Matrix Visual — Sales by Category and Region
10. Map — Sum of Sales by State
11. Treemap — Sum of Sales by Sub-Category
12. Gauge Chart — Total Profit

## Business Insights

**Insight 1:**
Technology is the highest revenue-generating category with over 
$0.7M in sales, making it the key driver of business growth.

**Insight 2:**
The West and East regions consistently outperform Central and 
South in both sales and profit, suggesting resource allocation 
should prioritize these regions.

**Insight 3:**
Sales show a strong upward trend from 2014 to 2017, indicating 
healthy business growth. However, discount rates above 0.4 
correlate with negative profit margins.
