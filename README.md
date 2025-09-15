# BDD-EXERCICE-TEST

SELECT 'title', 'rating' FROM film;
SELECT 'length' FROM film WHERE 'length' = 100 ;
SELECT title, `length` FROM film WHERE `length` > 50 ORDER BY length;
SELECT `customer_id`, rental_id , `rental_date` FROM rental WHERE cast(FROM_UNIXTIME('2005-05-28') AS datetime) GROUP BY rental_id, customer_id, return_date ORDER BY `return_date`;
SELECT rating, COUNT(`title`) FROM film GROUP BY `rating`;
SELECT `customer_id`, COUNT(rental_id) FROM rental WHERE `return_date` > "2005-05-28" GROUP BY customer_id HAVING(COUNT(rental_id)) > 2;
SELECT customer.customer_id, email, SUM(amount) FROM payment JOIN customer ON customer.customer_id = payment.customer_id GROUP BY customer_id ORDER BY SUM(amount) DESC LIMIT 10;
