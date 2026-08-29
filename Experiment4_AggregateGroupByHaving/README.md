# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

## Question 1
## CODE:


**Output:**

![Output1](output.png)

## Question 1
## CODE:

**Output:**

![Output2](output.png)

## Question 1
## CODE:

**Output:**

![Output3](output.png)

## Question 1
## CODE:


**Output:**

![Output4](output.png)

## Question 1
## CODE:

**Output:**

![Output5](output.png)

## Question 1
## CODE:

**Output:**

![Output6](output.png)

## Question 1
## CODE:

**Output:**

![Output7](output.png)

## Question 1
## CODE:

**Output:**

![Output8](output.png)

## Question 1
## CODE:

**Output:**

![Output9](output.png)

## Question 1
## CODE:

**Output:**

![Output10](output.png)


## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
