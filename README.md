# mysql-exercise


CREATE DATABASE my_company_database;
CREATE TABLE employees(
id INT AUTO_INCREMENT,
   	birth_date DATE,
   	last_name VARCHAR(100),
   	first_name VARCHAR(50),
   	gender VARCHAR(20),
   PRIMARY KEY(id)
);

ALTER TABLE employees ADD salary FLOAT(2);
ALTER TABLE employees ADD title VARCHAR(100);
ALTER TABLE employees ADD title_date DATE;

INSERT INTO employees (birth_date,last_name, first_name, gender, salary, title,title_date) values 
('1988-03-04', 'Smith', 'Klaus', 'male', '14000','Technic','2004-07-09'), 
('1995-03-04', 'Noriega', 'Jesy', 'female', '50000','Lead Engineer','2020-07-09'),
('1990-03-04', 'Roger', 'Roger', 'male', '24000','Junior Developer','2020-07-09'),
('2000-03-04', 'Peronni', 'Simone', 'male', '22000','Bussiness Core','2020-07-09'),
('1990-03-04', 'Varicova', 'Nadia', 'female', '27000','Scrum Master','2020-07-09'),
('1978-03-04', 'Jonshon', 'Mary', 'female', '30000','PO','2020-07-09'),
('1993-03-04', 'Gonzalez', 'Denise', 'female', '19000','Field Researcher','2018-07-09'),
('1994-03-04', 'Smith', 'Giorgia', 'female', '21000','Product Assistant','2021-07-09'),
('1997-03-04', 'Magodedov', 'Hashbulla', 'male', '44000','Comunity Manager','2023-07-09'),
('1999-03-04', 'Yurinov', 'Anna', 'female', '45000','CTO','2022-07-09'),
('1963-03-04', 'Dimaggio', 'Klaus', 'male', '34000','UX Leader','2013-07-09'),
('1991-03-04', 'Van Hoorne', 'Klaus', 'male', '24000','Hardware Assistant','2011-07-09'),
('1989-03-04', 'De la Villa', 'Klaus', 'male', '44000','Hardware Lead Engineer','2008-07-09'),
('1986-03-04', 'Castillo', 'Klaus', 'male', '24000','Developer','2019-07-09'),
('1995-03-04', 'Smith', 'Stan', 'male', '5000','Doorman','2013-07-09');




UPDATE employees SET salary = 23000 WHERE id = 1;


UPDATE employees SET first_name = 'Joan' WHERE id = 11 AND first_name = 'Klaus' AND last_name = 'Dimaggio' AND birth_date = '1963-03-04';


SELECT * FROM employees WHERE salary>20000;
SELECT * FROM employees WHERE salary<10000;
SELECT * FROM employees WHERE salary BETWEEN 14000 AND 50000;
SELECT COUNT(id) FROM employees;
SELECT * FROM employees WHERE title_date LIKE '2019%';
SELECT UCASE(first_name) FROM employees;
SELECT DISTINCT first_name FROM employees;

DELETE FROM employees WHERE id = 5;
DELETE FROM employees WHERE id AND salary > 20000





