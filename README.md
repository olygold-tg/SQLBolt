# РЕШЕНИЕ ЗДАНЙ ИЗ ТРЕНАЖЕРА SQLBolt
для помощи в решении можно ипользовать файл с 
## Урок SQL 1: ВЫБОР запросов 101
<details> 
  <summary>Решение</summary>

  1. Find the title of each film /Найдите название каждого фильма

```mysql
SELECT title FROM movies;
```

2. Find the director of each film / Найдите режиссера каждого фильма
   
```mysql
SELECT director FROM movies;
```

3. Find the title and director of each film / Найдите название и режиссера каждого фильма

```mysql
SELECT title, director FROM movies;
```
4. Find the title and year of each film / Найдите название и год выпуска каждого фильма 
```mysql
SELECT title, year FROM movies;
```
5. Find all the information about each film / Найдите всю информацию о каждом фильме

```mysql
SELECT * FROM movies;
```
</details>

## Урок 2 по SQL: Запросы с ограничениями (пункт 1)
<details> 
  <summary>Решение</summary>

1. Find the movie with a row id of 6 / Найдите фильм с идентификатором строки, равным 6

```mysql
SELECT * FROM movies
WHERE id = 6
```
2. Find the movies released in the years between 2000 and 2010 / Найдите фильмы, выпущенные в период с 2000 по 2010 год
   
```mysql
SELECT * FROM movies
WHERE year BETWEEN 2000 AND 2010
```
3. Find the movies not released in the years between 2000 and 2010 / Найдите фильмы, не вышедшие на экраны в период с 2000 по 2010 год
```mysql
SELECT * FROM movies
WHERE year NOT BETWEEN 2000 AND 2010
```

4. Find the first 5 Pixar movies and their release year/ Найдите первые 5 фильмов Pixar и год их выхода
```mysql
SELECT title, year 
FROM movies 
WHERE year <= 2003 
LIMIT 5
```
</details>

## Урок 3 по SQL: Запросы с ограничениями (Стр. 2)
<details> 
  <summary>Решение</summary>

1. Найдите все фильмы "Истории игрушек" / Найдите все фильмы из "Истории игрушек"
  ```mysql
SELECT * 
FROM movies 
WHERE Title 
LIKE '%Toy Story%';
```

2. Find all the movies directed by John Lasseter / Найдите все фильмы режиссера Джона Лассетера 

```mysql
SELECT * 
FROM movies 
WHERE director = 'John Lasseter'
```

3. Find all the movies (and director) not directed by John Lasseter / Найдите все фильмы (и режиссера), снятые не Джоном Лассетером

```mysql
SELECT Title, Director 
FROM movies 
WHERE Director != 'John Lasseter';
```

4. Find all the WALL-* movies / Найдите все фильмы на СТЕНЕ-*
```mysql
SELECT Title 
FROM movies 
WHERE Title LIKE '%WALL%';
```
</details>

## Урок 4 по SQL: Урок 4 по SQL: Фильтрация и сортировка результатов запроса
<details> 
  <summary>Решение</summary>
  
1. List all directors of Pixar movies (alphabetically), without duplicates / Составьте список всех режиссеров фильмов Pixar (в алфавитном порядке), без дублирования
```mysql
SELECT DISTINCT Director
FROM movies
ORDER BY Director
```

2. List the last four Pixar movies released (ordered from most recent to least) / Перечислите последние четыре фильма Pixar, вышедшие на экраны (в порядке возрастания от последнего к последнему).
```mysql
SELECT title
FROM movies
ORDER BY year DESC
LIMIT 4
```

3. List the first five Pixar movies sorted alphabetically / Перечислите первые пять фильмов Pixar, отсортированных в алфавитном порядке
```mysql
SELECT Title
FROM movies
ORDER BY Title ASC 
LIMIT 5
```

4. List the next five Pixar movies sorted alphabetically / Перечислите следующие пять фильмов Pixar, отсортированных в алфавитном порядке
```mysql
SELECT Title
FROM movies
ORDER BY Title ASC 
LIMIT 5
OFFSET 5
```
## Обзор SQL: Простые запросы ВЫБОРА
<details> 
  <summary>Решение</summary>

1. List all the Canadian cities and their populations /  Перечислите все канадские города и их население
```mysql
SELECT city, population  
FROM north_american_cities
WHERE country = 'Canada'
```
   
2. Order all the cities in the United States by their latitude from north to south / Расположите все города в Соединенных Штатах по их широте с севера на юг.
```mysql
SELECT city 
FROM north_american_cities
WHERE country = 'United States'
ORDER BY latitude DESC
```
3. List all the cities west of Chicago, ordered from west to east / Перечислите все города к западу от Чикаго, упорядоченные с запада на восток
```mysql
SELECT City, Longitude FROM north_american_cities
WHERE Longitude < -87.629798
ORDER BY Longitude ASC;
```

4. List the two largest cities in Mexico (by population) / Перечислите два крупнейших города Мексики (по численности населения).
```mysql
SELECT city, population
FROM north_american_cities
WHERE country = 'Mexico'
ORDER BY population DESC 
LIMIT 2
```

5. List the third and fourth largest cities (by population) in the United States and their population / Перечислите третий и четвертый по величине города (по численности населения) в Соединенных Штатах и их численность населения
```mysql
C
```
SELECT city, population
FROM north_american_cities
WHERE country = 'United States'
ORDER BY population DESC 
LIMIT 2 OFFSET 2;
```






```mysql

```
```mysql

```
```mysql

```
```mysql

```
```mysql

```
``mysql

```
```mysql

```
```mysql

```

</details>
