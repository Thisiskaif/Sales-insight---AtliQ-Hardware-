# Sales-insight-AtliQ-Hardware-

##### Is a company which supplies computer hardware and peripherals to many clients across India- The company has a head office in Dehli and regional offices throughout India.

## business issue:
The sales director is facing a lot of challenges like
The marketing is growing dynamically and then he’s struggling in terms of tracking the sales, needing more accurate insights about the company sales, and then take the necessary decisions.

## Imagine the scenario:

The sales director need to know how the sales are going in all operations and the information provided by the regional sales managers are not being enough.
Just hearing the numbers or receive tons of excel files is far from being effective in terms of having a reliable overview of the business.
Instead, he want to be able to  look at the data and understand what’s going on right away.

## Findings:
Extract the data from the source into MySQL workbench after a quick data exploration in MySQL, here are some initial findings:

• The database contains 5 tables: customers, date, markets, products, and transactions.

• There are 17 markets, 279 products, and 38 customers.

• The observation period is from january 2018 to june 2020.

• The total revenue in 2020 was $ 142,23 Mi, 42% less than 2019, which was $ 336,45 Mi.

• Most of the transactions data are in INR currency, but we have 4 records in U$ currency.

## ETL(Extract, Transform, Load)

Once I know the basic features of the data I have to work with, I imported the MySQL database into Power BI to do the necessary transformations and end up with a simple, reliable, and useful dashboard.
 ![image](https://user-images.githubusercontent.com/110671572/183743394-084c6d0d-bacd-439a-88e0-3213582809d0.png)

[sales transactions] — main table

TABLES CONNECTED
- sales customers > connected by “customer_code” column;
- sales date> connected by “date” column;
- sales products > connected by “product_code” column;
- sales markets > connected by “market_code” column.

## Measure created:
“Revenue” and “Sales Qty” measures to get the sum of each column instantly in the dashboard.

 ![image](https://user-images.githubusercontent.com/110671572/183744238-860392f0-5157-4cbb-a609-bc08204ade60.png)

## Filtering:

Filtering
Once the company is operating only in India, Ifiltered out “Paris” and “New York” in the sales markets table by unchecking the “(blank)” field in the “zone” column.

 ![image](https://user-images.githubusercontent.com/110671572/183744840-a42e3b00-e1f2-4e04-a28c-0d489918b831.png)

## Cleaning and adding columns:
- I find out that the “currency” column (sales transactions table) have 4 USD currency values, 2 of them with hidden characters, so i had to include an argument into the conditional formula, in order to create a new column called “norm_sales_amount”, where it converts the USD currency value into INR currency value.
- The “sales_amount” column has -1 and 0 values. I removed them in this case so we can see only the actual sales numbers on the dashboard (sometimes “0” means promotional sales and giveaways, but to know that, we should have further information, which is not the case of this project).

## Dashboards: 
After all the analysis and transformation, my data is reliable enough to build the dashboard.

## Total Sales:

![image](https://user-images.githubusercontent.com/110671572/183747780-d944d9f0-eacb-47d1-9e50-7b4d12db6912.png)

The dashboard shows all the main information about the company sales, such as Revenue, Sales Quantity,Revenue and Sales by Market, Revenue Trend, Top 5 Customers and Top 5 Products.
It can be filtered by YEAR and MONTH inside the observation period, so the sales director can have a deeper and quick view of the sales to support his decision making process.

## 2019:Revenue in terms of amount.
![image](https://user-images.githubusercontent.com/110671572/183749006-218c4600-5a93-4130-aab4-8773d35519c4.png)


## 2020: Revenue in terms of percentage.
![IMG_20220810_011332](https://user-images.githubusercontent.com/110671572/183750437-474c2761-82ba-4191-b413-1b7ca80b17a9.jpg)
