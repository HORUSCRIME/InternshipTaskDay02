# InternshipTaskDay02

Power BI Superstore Sales Dashboard
Overview
This repository contains a Power BI dashboard designed to analyze sales and profit performance of a Superstore dataset. The dashboard provides key insights into overall trends, geographical distribution, product category performance, customer segmentation, and the impact of discounts, enabling data-driven decision-making.
Dataset
The primary dataset used for this dashboard is superStore.csv. This dataset contains detailed information about sales transactions, including:
Order Information: Order ID, Order Date, Ship Date, Ship Mode
Customer Details: Customer ID, Customer Name, Segment
Product Details: Product ID, Category, Sub-Category, Product Name
Sales Metrics: Sales, Quantity, Discount, Profit
Geographical Information: Region, State, City, Postal Code, Country
Data Cleaning and Transformation
The raw superStore.csv dataset underwent a series of cleaning and transformation steps within Power BI's Power Query Editor to ensure data quality, consistency, and suitability for analysis.
The following steps were performed:
Data Loading:
The superStore.csv file was loaded into Power BI Desktop using the "Text/CSV" connector. Power BI's automatic delimiter and data type detection were reviewed.
Data Type Review and Correction:
Date Columns: Order Date and Ship Date columns were explicitly set to the "Date" data type to enable proper chronological analysis and date hierarchy creation.
Numerical Columns: Sales, Profit, Discount, and Shipping Cost (if present and used) were confirmed or converted to "Decimal Number" or "Fixed Decimal Number" to ensure accurate calculations.
Postal Code: Postal Code was set to "Text" to preserve leading zeros and prevent unintended numerical operations, as it functions more as an identifier than a measurable quantity.
Other Text Columns: All other categorical and descriptive columns (e.g., Category, Sub-Category, Region, Segment) were verified as "Text" data type.
Column Renaming (if applicable):
Column names were reviewed and made more user-friendly and consistent (e.g., ensuring spaces for readability if they were originally snake_case or similar).
Handling Missing Values (if any):
A check for null or blank values was performed across critical columns. For the Superstore dataset, this is typically not a major issue, but if any were found, strategies like removal of rows, replacement with default values, or imputation would have been considered.
Creation of New Calculated Columns:
Profit Ratio: A custom column named Profit Ratio was created using the formula [Profit] / [Sales]. This provides a normalized measure of profitability.
Date Components: New columns were extracted from Order Date to facilitate time-based analysis:
Order Year (extracted year from Order Date)
Order Month (extracted month name from Order Date)
Order Quarter (extracted quarter of the year from Order Date)
These new columns enable flexible analysis across different time granularities without relying solely on Power BI's default date hierarchy.
These data cleaning and transformation steps ensure that the dataset is robust, accurate, and ready for effective visualization and analysis within the Power BI dashboard.
Dashboard Features
The Power BI dashboard provides the following key analytical views:
Executive Summary (Page 1):
Key Performance Indicators (KPIs): Displays total sales, total profit, and profit ratio for a quick overview of performance.
Sales & Profit Trend: A line chart illustrating the historical trends of sales and profit over time, allowing for drill-down by year, quarter, and month.
Geographical Sales Distribution: A map visual showing sales performance across different states/regions.
Product & Customer Deep Dive (Page 2):
Sales by Product Category: A column chart breaking down sales performance by main product categories.
Profit by Sub-Category: A bar chart highlighting profit contribution by sub-category, potentially with conditional formatting to identify underperforming or loss-making sub-categories.
Sales by Customer Segment: A donut chart showcasing the distribution of sales across different customer segments.
Profit vs. Discount: A scatter plot to analyze the relationship between the discount applied and the resulting profit, helping to identify optimal discounting strategies.
Sales by Shipping Mode: A pie/donut chart showing the distribution of sales across various shipping modes.
How to Use
Clone the Repository:
git clone [repository-url]


Open in Power BI Desktop:
Navigate to the cloned directory.
Open the .pbix file (the Power BI Desktop file) using Power BI Desktop.
Refresh Data (if necessary):
If the dataset superStore.csv is updated or moved, you might need to refresh the data source. Go to Home tab -> Refresh.
Explore the Dashboard:
Utilize the slicers (e.g., Order Date, Region, Category, Segment) to filter the data and explore specific insights.
Click on different elements within charts to see how other visuals interact and highlight related data points.
Navigate between "Page 1" and "Page 2" using the page tabs at the bottom.
Future Enhancements
Drill-through Pages: Implement drill-through functionality to allow users to click on a specific data point (e.g., a sub-category) and navigate to a detailed page showing individual orders or products within that selection.
Advanced DAX Measures: Develop more complex DAX measures for metrics like Year-over-Year Growth, Customer Lifetime Value, or distinct counts.
What-If Analysis: Integrate parameters for "what-if" scenarios, such as analyzing the impact of different discount percentages on overall profit.
Row-Level Security: If sharing with different stakeholders, implement row-level security to restrict data visibility based on user roles.
Dashboard Accessibility: Enhance accessibility features for users with disabilities.
