#Customers and Products Analysis

The tool used for analysis is SQL Browser for SQLite. 

The SQL script contains: JOINs, CTEs, UNION set operator, aliases for columns, tables and queries, calculated columns, subqueries, data transformation using CAST, ROUND functions, among others.

This project analyzes data from a sales records database for scale model cars and extracts KPIs and other information for decision-making, aimed at increasing sales and reducing certain types of operational risk/increasing efficiency with regards to sales performance and customer experience. It seeks to obtain answers for the following questions:
i.	Which products should we order more of or less of?
ii.	How should we tailor marketing and communication strategies to customer behaviors?
iii.	How much can we spend on acquiring new customers?

We begin with EDA to gain a better understanding of the data. For instance, we used PRAGMA() to get table information. To select each table name (from the database) as a string, we used:
*SELECT name AS table_name
  FROM sqlite_schema
 WHERE type='table'*

We found out which products to order more/less of using the KPIs low_stock & product_performance. Priority products for restocking are those with high product performance that are on the brink of being out of stock. The results showed that the productLine for Classic cars was more popular & fast-moving.

Secondly, we explored customer information to find the VIP customers & those who are less engaged so we could have targeted campaigns. *Ceteris paribus*, an assumption is made that VIP customers bring in more profit while less-engaged customers bring in less profit. Based on this, next courses of action included organizing some events to drive loyalty for the VIPs and launching a campaign for the less engaged. 

Lastly, we determined the estimate amount of money that could be used to acquire new customers. Since the number of customers had been reducing significantly, the store hadn’t had new customers in a long while, more marketing was necessary. To do this, we computed the Customer Lifetime Value (LTV), which represents the average amount of money a customer generates. The LTV was about $ 39039.59 & if the business got 10 new customers in the following year, we could estimate the earnings to have increased by $ 390395.90

***It then goes without saying……” you spend money to get money (where it’s worth it)!”***

