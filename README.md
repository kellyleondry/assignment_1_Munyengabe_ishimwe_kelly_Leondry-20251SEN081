# assignment_1_Munyengabe_ishimwe_kelly_Leondry-20251SEN081
## PLSQL Assignment One - Sunrise Supermarket

NAMES: MUNYENGABE ISHIMWE Kelly Leondry
STUDENT ID: 20251SEN081

# 1. Business Scenario
Sunrise Supermarket sells products to customers, who place orders containing one or more items. 
Management wants to understand who their customers are, what they buy, and how sales are trending over time. Populate the tables with at least 5 customers, 8 products across at least 3 categories, 15 orders, and 25 order items across multiple dates.

# 2. Activity Dane About the Scenario(Summary)
By the use SQL Shell(psql) I created the Sunrise Supermarket database with four tables: customers, products, orders, and order items. I defined their primary and foreign keys, then inserted sample data consisting of customers, products, orders, and order items.

After creating and populating the database, I used JOIN queries to combine customer, order, and product information. I then used a CTE to calculate each customer's total spending and identify customers spending above the average.

Finally, I used window functions such as RANK(), ROW_NUMBER(), SUM() OVER, and LAG() to rank customers, number their orders, calculate running revenue, and find the number of days between customer orders. This demonstrated how SQL can be used to analyze supermarket data and support business decisions.

# 3. # JOIN queries
1. JOIN Query 1 Display every order together with the customer's name, city, and order
date.

Query

SELECT
    o.order_id,
    c.customer_name,
    c.city,
    o.order_date
FROM orders o
INNER JOIN customers c
    ON o.customer_id = c.customer_id;
    as shown here [JOIN query 1](https://www.google.com)


