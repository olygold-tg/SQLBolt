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

``````mysql

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
```mysql

```
```mysql

```
```mysql

```

</details>
