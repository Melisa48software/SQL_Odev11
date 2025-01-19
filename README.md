# SQL_Odev11
lcw bootcamp sql 11.ödev reposudur.

-- 1. Actor ve Customer Tablo'larındaki first_name Sütunundaki Tüm Verileri Sıralamak
SELECT actor.first_name
FROM actor
UNION
SELECT customer.first_name
FROM customer;

-- 2. Actor ve Customer Tablo'larındaki first_name Sütunlarındaki Kesişen Verileri Sıralamak
SELECT actor.first_name
FROM actor
INTERSECT
SELECT customer.first_name
FROM customer;

-- 3. Actor Tablosunda Bulunan Ancak Customer Tablosunda Bulunmayan first_name Verilerini Sıralamak
SELECT actor.first_name
FROM actor
EXCEPT
SELECT customer.first_name
FROM customer;

-- 4. İlk 3 Sorgu İçin Tekrar Eden Veriler (UNION ALL kullanarak)
-- Tüm Veriler
SELECT actor.first_name
FROM actor
UNION ALL
SELECT customer.first_name
FROM customer;

-- Kesişen Veriler
SELECT actor.first_name
FROM actor
INTERSECT
SELECT customer.first_name
FROM customer;

-- Actor Tablosunda Bulunan Ancak Customer Tablosunda Bulunmayan Veriler
SELECT actor.first_name
FROM actor
EXCEPT
SELECT customer.first_name
FROM customer;

