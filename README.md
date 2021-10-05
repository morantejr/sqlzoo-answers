# sqlzoo-answers
Solutions for [sqlzoo.com](https://sqlzoo.net/wiki/SQL_Tutorial) from levels 1-10 (minus 9+ COVID-19 level)

# Table of Contents
0 - [SELECT basics](#select-basics)


## SELECT basics
Some simple queries to get you started

1.
```sql
  SELECT population FROM world
    WHERE name = 'Germany'
```
2.
```sql
  SELECT name, gdp/population FROM world
    WHERE area > 5000000
```
3.
```sql
  SELECT name, population FROM world
    WHERE name IN ('Ireland','Iceland','Denmark');
```
4.
```sql
  SELECT name, area FROM world
    WHERE area BETWEEN 200000 AND 250000
```
