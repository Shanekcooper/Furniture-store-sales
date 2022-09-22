# Furniture-store-sales
This project focused on sales for the month of January across all locations.

SELECT name, SUM(price) AS total_spend FROM sales GROUP BY name ORDER BY total_spend DESC;

SELECT product, Count(*) AS total FROM sales GrOUP by product;

SELECT payment_type, count(*) AS paymenttype_total FROM sales GROUP BY payment_type;

SELECT country, count(*) As total FROM sales GROUP BY country ORDER by total DESC;

SELECT Product, AVG(price) AS avg_sales FROM sales GROUP BY product;

SELECT name, SUM(price) AS total_spend FROM sales GROUP BY name HAVING total_spend <= 1200;

SELECT * FROM sales WHERE country ="United states";

SELECT * FROM sales WHERE state="NY" OR state= "FL";

SELECT transaction_date,name, product FROM sales WHERE country= "United states" AND product = "Chair" OR product = "Couch";

SELECT state, count(*) AS state_count FROM sales GROUP BY state;

SELECT state, count(*) AS state_count,
CASE
  WHEN count(*) >= 5 THEN "green_zone" ELSE "red_zone"
    END AS zone
      FROM sales GROUP BY state ORDER BY state_count DESC;
