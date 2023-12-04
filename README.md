# Lab10
## Answers 
SELECT CustomerName FROM Customers WHERE country = 'UK';

SELECT productName, unit, price FROM products WHERE price >= 55;

SELECT Products.ProductName, Products.Price, Categories.CategoryName FROM Products INNER JOIN Categories ON Products.CategoryID = Categories.CategoryID WHERE Categories.CategoryName = 'Beverages' ORDER BY Products.Price ASC;

SELECT Employees.FirstName, Employees.LastName, Orders.OrderID FROM (Employees INNER JOIN Orders ON Employees.EmployeeID = Orders.EmployeeID) WHERE Employees.EmployeeID BETWEEN 1 AND 5 ORDER BY Employees.LastName ASC;

SELECT Customers.CustomerName, Orders.OrderID, Products.ProductName, OrderDetails.Quantity FROM ((Customers INNER JOIN Orders ON Customers.CustomerID = Orders.CustomerID) INNER JOIN OrderDetails ON Orders.OrderID = OrderDetails.OrderID) INNER JOIN Products ON OrderDetails.ProductID = Products.ProductID ORDER BY Customers.CustomerName ASC;
