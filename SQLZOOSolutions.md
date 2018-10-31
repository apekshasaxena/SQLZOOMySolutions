### 1. SELECT basics
### 2. SELECT from world
### 3. SELECT from nobel
### 4. SELECT in SELECT
### 5. SUM and COUNT
### 6. JOIN
### 7. More JOIN
### 8. Using NULL
### 9. Self JOIN
---

### 1. SELECT basics

1. 
```sql
SELECT population
FROM world
WHERE name = 'Germany';
```

2. 
```sql
SELECT name, population
FROM world
WHERE name IN ('Sweden', 'Norway', 'Denmark');
```

3.
```sql
SELECT name, area
FROM world
WHERE area BETWEEN 200000 AND 250000;
```
---

### 2. SELECT from world

1.
```sql
SELECT name, continent, population 
FROM world;
```

2.
```sql
SELECT name 
FROM world
WHERE population >= 200000000;
```

3.
```sql
SELECT name, (gdp/population) as per_capita_gdp
FROM world
WHERE population >= 200000000;
```

4.
```sql
SELECT name, (population/1000000)
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
SELECT name, population, area
FROM world
WHERE (area > 3000000 OR population > 250000000) AND NOT(area > 3000000 AND population > 250000000);
```

9.
```sql
SELECT name, round(population/1000000,2), round(gdp/1000000000,2)
FROM world
WHERE continent = 'South America';
```

10.
```sql
SELECT name, round(gdp/population, -3)
FROM world
WHERE gdp >= 1000000000000;
```

11.
```sql
SELECT name, capital
FROM world
WHERE LENGTH(name) = LENGTH(capital);
```

12.
```sql
SELECT name, capital
FROM world
WHERE LEFT(name,1) = LEFT(capital,1) AND name <> capital;
```

13.
```sql
SELECT name
FROM world
WHERE name LIKE '%a%' 
      AND name LIKE '%e%' 
      AND name LIKE '%i%' 
      AND name LIKE '%o%' 
      AND name LIKE '%u%'
      AND name NOT LIKE '% %';
```
---


