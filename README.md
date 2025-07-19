Retail Store Sales Analysis

Overview

The Dirty Retail Store Sales dataset contains 12,575 rows of synthetic data representing sales transactions from a retail store.
The dataset includes eight product categories with 25 items per category, each having static prices. 
It is designed to simulate real-world sales data, including intentional "dirtiness" such as missing or inconsistent values. 
This dataset is suitable for practicing data cleaning, exploratory data analysis (EDA), and feature engineering.

File Information

•	File Name: retail_store_sales.csv
•	Number of Rows: 12,575
•	Number of Columns: 11

Column Description

•	Transaction ID 	: A unique identifier for each transaction. Always present and unique. 	
•	Customer ID:	A unique identifier for each customer. 25 unique customers. 	
•	Category:	The category of the purchased item.
•	Item:	The name of the purchased item. May contain missing values or None. 	
•	Price Per Unit: 	The static price of a single unit of the item. May contain missing or None values.
•	Quantity:	The quantity of the item purchased. May contain missing or None values. 
•	Total Spent:	The total amount spent on the transaction. Calculated as Quantity * Price Per Unit. 	
•	Payment Method:	The method of payment used. May contain missing or invalid values. 	Cash, Credit Card
•	Location: 	The location where the transaction occurred. In-store, Online
•	Transaction Date:	The date of the transaction. Always present and valid. 
•	Discount Applied: 	Indicates if a discount was applied to the transaction. 

TOOLS FOR ANALYSIS

•	Power BI
•	Power Query

DATA CLEANING

•	Check for duplicate
•	Change ‘Transaction date’ datatype to DateTime
•	Used the ‘Remove Error’ function in power query to filter out the blanks in the dataset
•	Removed the ‘Discount Applied’ column because of it scantiness 

ANALYSIS

DAX Formular/Measures:

•	Total Sales
Total sales = SUM(Retail store sales[Total spent])

•	Total Quantity Sold
	Total Quantity Sold = SUM(Retail store sales[Quantity])

•	Average Order Value
	Average Order Value = DIVIDE(Retail store sales[Total sales],[ Total Quantity Sold])

•	Order Count
Order Count = COUNT(Retail store sales[Transaction ID])

DASHBORD

![Image alt](https://github.com/lanrekareem/Retail-store-sales-Analysis/blob/main/Hajia%20Fadeelah%20Retail%20store%20Dashboard.png?raw=true)



 Key Insights

1. Order Volume & Sales Performance

•	Total Orders: 11K
•	Total Sales: ₦1.5M
•	Average Order Value (AOV): ₦23.42

Insight: While order volume is high, the average order value is relatively low. This suggests customers are placing many small-value orders.

Recommendation: Introduce bundle deals or minimum order value discounts to encourage higher spending per transaction.

 2. Popular Payment Method

•	Fairly even split among:

o	Cash: 32.46%
o	Credit Card: 34.87%
o	Digital Wallet: 32.66%

Insight: No single payment method dominates, indicating customers are flexible in how they pay.

Recommendation:

•	Maintain all three options.
•	Consider incentivizing digital payments (e.g. cashback, points) to reduce cash handling risks and improve tracking.

3. Sales by Product Category

Top categories by sales:

•	Beverages
•	Furniture
•	Food
•	Electric Household Items
•	Computers & Accessories

Insight: Beverages and furniture are the top-selling categories. Lower-performing ones include Milk Products and Butchers.

Recommendation:

•	Double down on promotions for top-selling categories.
•	Put up slow-moving items for potential discounts or product delisting.
•	milk products are underperforming because of it perishability.

4. Sales by Location

•	Online: ₦749.43K
•	In-store: ₦723.57K

Insight: Online sales slightly outperform in-store sales.

Recommendation:

•	Strengthen the online sales channel via marketing and user experience improvements.
•	Consider adding click-and-collect or home delivery options.
•	Compare customer demographics across channels for more targeted campaigns.


5. Sales Trend Over Time

•	Sales fluctuate across 2022–2025.
•	Sudden drop at the end of 2025.

Insight: There's an upward trend but a sharp decline recently, possibly due to missing or incomplete data for the current year.

Recommendation:
•	Plan seasonal promotions during low-performing months.


6. Top Customers

•	Top spender: CUST_24 – ₦64,608.00 across 489 orders.
•	High loyalty base: Most top customers placed 440–490 orders.

Insight: Strong customer retention is evident with many repeat buyers.

Recommendation:

•	Launch a loyalty program to reward frequent shoppers.



