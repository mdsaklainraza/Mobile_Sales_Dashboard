Objective:

This project presents an interactive Mobile Sales Dashboard developed in Power BI. 
It provides a comprehensive analysis of mobile sales performance across various dimensions 
including monthly sales trends, transaction counts, average pricing, and popular mobile brands and models. 
The dashboard enables users to drill down into sales data by city, month, payment method, and other key indicators to help stakeholders make data-driven decisions.

DAX Formula:

Total_Sales = SUMX(Sales_Data,Sales_Data[Units Sold]*Sales_Data[Price Per Unit])

Avg_Price = AVERAGE(Sales_Data[Price Per Unit])

Total_Quantity = SUM(Sales_Data[Units Sold])

Transaction = COUNTROWS(Sales_Data)

Same Period Last Year = CALCULATE([Total_Sales],
SAMEPERIODLASTYEAR(Custom_Date[Date].[Date]))

Sales = Sales_Data[Units Sold]*Sales_Data[Price Per Unit]

Rating Status = IF(Sales_Data[Customer Ratings]>=4,"Good",IF(Sales_Data[Customer Ratings]>2,"Average","Poor"))

MTD = TOTALMTD([Total_Sales],Custom_Date[Date].[Date])

Insights:

Total Sales and Quantity: Showcases cumulative sales and quantity metrics, with detailed breakdowns by month and city.

Top Performing Brands and Models: Visualizes sales distribution across popular mobile brands and models, highlighting key contributors to revenue

Sales by Payment Method: Illustrates customer payment preferences (UPI, Credit Card, Debit Card, Cash), which can aid in tailoring payment options.

Time-based Sales Analysis: Provides insights into daily and monthly sales patterns, enabling strategic planning around peak sales periods.

Customer Ratings: Offers a breakdown of customer satisfaction levels, providing a view into product performance and quality.

Month-to-Date (MTD) and Quarterly Analysis: The MTD and quarterly views allow for quick performance checks during the month or
quarter, making it easier to track progress against targets and make adjustments in real time

This dashboard aids in tracking key metrics in real-time, understanding customer preferences, and identifying high-performing regions, helping to drive targeted marketing and inventory planning strategies.
