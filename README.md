# SQL---DEV-3
Sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştirilmiştir.
--country tablosunda bulunan country sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız
SELECT * FROM country 
WHERE country LIKE 'A%a';

--country tablosunda bulunan country sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.
SELECT * FROM country 
WHERE country LIKE '%n';

--film tablosunda bulunan title sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri içeren film isimlerini sıralayınız.
SELECT  title FROM film 
WHERE title ILIKE '%T%'

--film tablosunda bulunan tüm sütunlardaki verilerden title 'C' karakteri ile başlayan veuzunluğu (length) 90 dan büyük olan ve rental_rate 2.99 olan verileri sıralayınız
SELECT title, length, rental_rate FROM film
WHERE title  LIKE 'C%' AND length > 90 AND rental_rate =2.99 ;
