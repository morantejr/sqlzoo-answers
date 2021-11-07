# sqlzoo-answers
Solutions for [sqlzoo.com](https://sqlzoo.net/wiki/SQL_Tutorial) from levels 1-10 (minus 9+ COVID-19 level)

# Table of Contents
0. [SELECT basics](#select-basics)
1. [SELECT name](#select-name)
2. [SELECT from world](#select-from-world)

## SELECT basics
Some simple queries to get you started

1.
```sql
  SELECT population FROM world
    WHERE name = 'Germany'
```
2.
```sql
  SELECT name, population FROM world
    WHERE name IN ('Sweden', 'Norway', 'Denmark');
```
3.
```sql
  SELECT name, area FROM world
    WHERE area BETWEEN 200000 AND 250000;
```

## SELECT name
Some pattern matching queries

1.
```sql
  SELECT name FROM world
    WHERE name LIKE 'Y%';
```

2.
```sql
SELECT name FROM world
  WHERE name LIKE '%y';
```

3.
```sql
  SELECT name FROM world
    WHERE name LIKE '%x%';
```

4.
```sql
  SELECT name FROM world
    WHERE name LIKE '%land';
```

5.
```sql
   SELECT name FROM world
     WHERE name LIKE 'C%' AND name LIKE '%ia';
```

6.
```sql
SELECT name FROM world
  WHERE name LIKE '%oo%'
```

7.
```sql
SELECT name FROM world
  WHERE name LIKE '%a%a%a%';
```

8.
```sql
SELECT name FROM world
 WHERE name LIKE '_t%'
ORDER BY name;
```

9.
```sql
SELECT name FROM world
 WHERE name LIKE '%o__o%';
```

10.
```sql
SELECT name FROM world
 WHERE name LIKE '____';
```

11.
```sql
SELECT name
  FROM world
 WHERE name = capital;
```

12.
```sql
SELECT name
  FROM world
 WHERE capital = concat(name, ' City');
```

13.
```sql
SELECT capital, name
  FROM world
WHERE capital LIKE concat('%', name, '%');
```

14.
```sql
SELECT capital, name
  FROM world
WHERE capital LIKE concat('%', name, '%') AND capital > name;
```

15.
```sql
SELECT name, REPLACE(capital, name, '')
  FROM world
  WHERE capital LIKE concat('%', name, '%') AND capital > name;
```
## SELECT from world
In which we query the World country profile table.

1.
```sql
  SELECT name, continent, population 
  FROM world;
```

2.
```sql
SELECT name FROM world
  WHERE population >= 200000000;
```

3.
```sql
SELECT name, GDP/population
  FROM world
  WHERE population >= 200000000;
```

4.
```sql
SELECT name, population/1000000
  FROM world
  WHERE continent = 'South America';
```

5.
```sql
SELECT name, population
FROM world
WHERE name IN ('France', 'Germany', 'Italy');
```

6.
```sql
SELECT name
  FROM world 
  WHERE name LIKE '%United%';
```

7.
```sql
SELECT name, population, area
  FROM world
  WHERE area > 3000000 OR population > 250000000;
```

8.
```sql
SELECT name, population, area FROM world
WHERE area > 3000000 XOR population > 250000000
```

9.
```sql
SELECT name, ROUND(population/1000000,2),ROUND(GDP/1000000000,2) continent
FROM world
WHERE continent = 'South America';
```

10.
```sql
SELECT name, ROUND(GDP/population,-3)
FROM world
WHERE GDP >= 1000000000000
```

11.
```sql
SELECT name, capital
  FROM world
 WHERE length(name) = length(capital);
```

12.
```sql
SELECT name
  FROM world
 WHERE capital = concat(name, ' City');
```

13. 
```sql
SELECT capital, name
  FROM world
WHERE capital LIKE concat('%', name, '%');
```
