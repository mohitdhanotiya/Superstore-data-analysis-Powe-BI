# Superstore-data-analysis-Powe-BI
- Power BI dashboards can be a helpfull tool to provide insights into sales performance and trends of an organization.
- The dashboard should include key metrics such as total sales, sales by product, sales by location, sales by customer segment, and sales by product category.
- It should also provide comparisons of performance to prior years, and allow for drill-down into individual market and products.

### Table of Content
- Problem Statement
- Importing Data
- Data Preparation
- DAX
- Data Visualization/Report

### Problem Statement:
Build a Sales Analysis, Product Analysis and Shipping Analysis Dashboard.

##### Tools Used:
Microsoft Power BI

### Importing Data
Dataset was downloaded from Kaggle and then import into Power BI desktop.

### Data Preparation
Dataset was loaded into Power BI , Data was tranformed and loaded in Power Query editor.

- Validation of each coloumn Data Type's
- Removing Unnecessary Row's and Column's
- Created custom column using M code in power query
- Created Date table using M code.

### DAX
- CY sales = 
var CY = MAX(Orders_All[Year])
Return
CALCULATE(SUM(Order_Details[Sales]),Orders_All[Year]=CY)

- PY sales = 
var PY = MAX(Orders_All[Year])-1
Return
CALCULATE(SUM(Order_Details[Sales]),Orders_All[Year]=PY)

- YOY Sales growth % = DIVIDE([CY sales]-[PY sales],[PY sales],BLANK())
- Shipping cost per order = SUM(Orders_All[Shipping Cost])/COUNT(Orders_All[Order ID])
- Profit % = SUM(Order_Details[Profit])/SUM(Order_Details[Sales])
- Discount value = SUM(Order_Details[Original Markup])-SUM(Order_Details[Sales])
- Discount % = Order_Details[Discount value]/SUM(Order_Details[Original Markup])

### Data Visualization/Report
- Area chart to show trends
- Line and clustered column chart to show YOY sales growth %
- Scatter plot
- Bar chart
- Column Chart
- Pie Chart
- Use of M code in Advanced editor of power query to import images
- Decomposition Tree
- Conditional formatting
- Sparklines
- Use of bookmarks and buttons to navigate into the report
- Tooltip and many more functions...

