# Task-7-Creating-Views

CREATE TABLE employees (
emp_id INT PRIMARY KEY,
name VARCHAR(50),
department VARCHAR(50),
salary DECIMAL(10, 2),
joining_date DATE
);

CREATE VIEW high_salary_employees AS
SELECT
emp_id,
name,
department,
salary,
YEAR(joining_date) AS join_year
FROM employees
WHERE salary > 50000
ORDER BY salary DESC;

CREATE VIEW public_employee_list AS
SELECT
name,
department
FROM employees;

SELECT * FROM high_salary_employees;

