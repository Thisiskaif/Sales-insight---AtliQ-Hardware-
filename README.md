# Sales-insight-AtliQ-Hardware-

##### Is a company which supplies computer hardware and peripherals to many clients across India- The company has a head office in Dehli and regional offices throughout India.

## business issue:
The sales director is facing a lot of challenges like
The marketing is growing dynamically and then he’s struggling in terms of tracking the sales, needing more accurate insights about the company sales, and then take the necessary decisions.

# Imagine the scenario:

The sales director need to know how the sales are going in all operations and the information provided by the regional sales managers are not being enough.
Just hearing the numbers or receive tons of excel files is far from being effective in terms of having a reliable overview of the business.
Instead, he want to be able to  look at the data and understand what’s going on right away.

# Findings:
Extract the data from the source into MySQL workbench after a quick data exploration in MySQL, here are some initial findings:

• The database contains 5 tables: customers, date, markets, products, and transactions.

• There are 17 markets, 279 products, and 38 customers.

• The observation period is from january 2018 to june 2020.

• The total revenue in 2020 was $ 142,23 Mi, 42% less than 2019, which was $ 336,45 Mi.

• Most of the transactions data are in INR currency, but we have 4 records in U$ currency.

# ETL(Extract, Transform, Load)

Once I know the basic features of the data I have to work with, I imported the MySQL database into Power BI to do the necessary transformations and end up with a simple, reliable, and useful dashboard.
# ![image](https://user-images.githubusercontent.com/110671572/183743394-084c6d0d-bacd-439a-88e0-3213582809d0.png)

[sales transactions] — main table

TABLES CONNECTED
- sales customers > connected by “customer_code” column;
- sales date> connected by “date” column;
- sales products > connected by “product_code” column;
- sales markets > connected by “market_code” column.

# Measure created:
“Revenue” and “Sales Qty” measures to get the sum of each column instantly in the dashboard.
