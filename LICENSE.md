answer.sql file.
NO 1
USE sales;
SELECT employees.firstName,employees.lastName,employees.email,employees.officeCode
FROM employees
INNER JOIN offices
ON EMPLOYEES.officeCode=offices.officeCode;

NO 2
USE sales;
SELECT products.productName,products.productVendor,products.productLine
FROM products
LEFT JOIN productlines
ON products.productLine=productlines.productLine;

NO 3
USE sales;
SELECT customers.customerName,orders.orderDate,orders.status
FROM customers
RIGHT JOIN orders
ON customers.customerNumber=orders.customerNumber
LIMIT 10;
