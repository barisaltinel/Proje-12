city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.

-- 1) city ve country isimlerini birlikte gösteren INNER JOIN
SELECT
  ci.city,
  co.country
FROM city AS ci
INNER JOIN country AS co
  ON ci.country_id = co.country_id
ORDER BY co.country, ci.city;

-- 2) payment_id ile customer’ın first_name ve last_name’ini birlikte gösteren INNER JOIN
SELECT
  p.payment_id,
  c.first_name,
  c.last_name
FROM payment AS p
INNER JOIN customer AS c
  ON p.customer_id = c.customer_id
ORDER BY p.payment_id;

-- 3) rental_id ile customer’ın first_name ve last_name’ini birlikte gösteren INNER JOIN
SELECT
  r.rental_id,
  c.first_name,
  c.last_name
FROM rental AS r
INNER JOIN customer AS c
  ON r.customer_id = c.customer_id
ORDER BY r.rental_id;
