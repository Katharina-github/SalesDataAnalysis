# SalesDataAnalysis

In 2020, a hypotetical dynamic online shop specializing in plans and accessories was founded in Germany. With a focus on quality and customer satisfaction, the shop quickly gained traction and expanded its operations to the Netherlands shortly after. Buoyed by its success, the shop ventured into Southern Europe, establishing a presence in Spain and Italy. Most recently, the shop expanded to the UK and Ireland, marking its entry into the English-speaking market.
This project aims to analyze the shop's sales performance, customer behavior, and operational efficiency using a synthetic database that simulates real-world scenarios.

1.	Goal and key questions of the analysis

Objective of the Analysis

•	Main Goal: Increase profit by optimizing sales strategies, reducing costs, and improving customer satisfaction.

•	Key Questions:

o	Which products and categories have the highest profit margins?

o	Are there underperforming products or regions that need attention?

o	How can we reduce costs (e.g., shipping, returns) without compromising customer satisfaction?

o	Which customer segments are most profitable, and how can we target them better?

This project seeks to uncover actionable insights from the synthetic data, including:

•	Sales Performance: Identify top-performing products, categories, and regions.

•	Customer Insights: Understand customer behavior, preferences, and loyalty.

•	Inventory Efficiency: Analyze inventory management practices and their impact on sales.

•	Marketing Effectiveness: Evaluate the success of marketing campaigns in driving sales.

•	Returns Analysis: Investigate the reasons behind returns and their impact on profitability.

2.	 Sythetical dataset

The database includes the following tables:
1.	products_df: Contains information about the products, including categories, popularity scores, and pricing.
2.	customers_df: Stores customer details such as demographics, loyalty scores, segments (retail vs. wholesale), and buying preferences.
3.	sales_df: Records all sales transactions, including product IDs, customer IDs, sales amounts, and dates.
4.	returns_df: Tracks returned items, including reasons for returns and associated product categories.
5.	campaigns_df: Documents marketing campaigns and their impact on sales in specific regions.
6.	inventory_df: Manages stock levels, reorder points, and inventory replenishment.
7.	not_realized_purchases_df: Captures failed purchase attempts due to insufficient inventory.
8.	inventory_snapshots_df: Contains two snapshots of the stock levels of the products per day
   
Key Features of the Synthetic Data

To ensure the data reflects real-world dynamics, the following features were incorporated:

1.	Seasonal influence:
o	General seasonality: Sales fluctuate based on the time of year, with variations across countries.
o	Product category seasonality: Certain product categories experience higher demand during specific seasons.

2.	Product popularity:
o	Products are assigned a popularity score, which influences their sales frequency. Popular products are sold more often.

3.	Customer behavior:
o	Segmentation: Customers are divided into retail and wholesale segments, each with distinct buying behaviors.
Retail customers: Tend to buy smaller quantities but more frequently.
Wholesale customers: Purchase larger quantities but less frequently.
o	Price sensitivity: Products with high prices are purchased in lower quantities.
o	Age preferences: Customers exhibit buying preferences based on their age.
o	Loyalty scores: Customers with higher loyalty scores purchase more frequently.

4.	Marketing campaigns:
o	The shop launched different marketing campaigns, each designed to boost sales in a specific country for a limited time. These campaigns are reflected in the campaigns_df table.

5.	Inventory management:
o	The sales_df and inventory_df tables are interconnected. When a sale occurs, the inventory is reduced.
o	If inventory levels fall below the reorder point, new stock is added to prevent shortages.
o	Sales that cannot be fulfilled due to insufficient inventory are recorded in the not_realized_purchases_df table.
o	The stock levels of the products are recorded twice a day (before and after restocking)

6.	Returns:
o	The likelihood of returns is influenced by the product category. For example, certain categories may have higher return rates due to customer dissatisfaction or product defects.
