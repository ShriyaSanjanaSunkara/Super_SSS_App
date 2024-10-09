# Assignment 4
### SQL JOINS
## Customers Table

| customer_id | customer_name |
|-------------|---------------|
| 1           | Shriya        |
| 2           | Sanjana       |

## Orders Table

| order_id | customer_id | product_name | order_date |
|----------|-------------|--------------|------------|
| 1        | 1           | Laptop       | 2024-10-01 |
| 2        | 1           | Mouse        | 2024-10-02 |
| 3        | 2           | Keyboard     | 2024-10-03 |

## Products Table

| product_id | product_name |
|------------|--------------|
| 1          | Laptop       |
| 2          | Mouse        |
| 3          | Keyboard     |

## Suppliers Table

| supplier_id | supplier_name    |
|-------------|------------------|
| 1           | Tech Supply LTD  |
| 2           | Gadget Planet    |

## Product-Suppliers Table

| product_id | supplier_id |
|------------|-------------|
| 1          | 1           |
| 2          | 2           |
| 3          | 1           |

# a)Inner Join: Customers and Orders

| customer_name | product_name |
|---------------|--------------|
| Shriya        | Laptop       |
| Sanjana       | Mouse        |
| Shriya        | Mouse        |

# b) LEFT JOIN: Customers and Orders

| customer_name | product_name |
|---------------|--------------|
| Shriya        | Laptop       |
| Sanjana       | Mouse        |
| Shriya        | Mouse        |
| John          | NULL         |

# c) RIGHT JOIN (Emulated with LEFT JOIN): Products and Suppliers

| product_name | supplier_name    |
|--------------|------------------|
| Laptop       | Tech Supply LTD  |
| Mouse        | Gadget Planet    |
| Keyboard     | NULL             |
| NULL         | Gadget Planet    |

# f) Cross Join : Products and Customers

The table shows all possible combinations of product names and customer names between the `products` and `customers` tables.

| product_name | customer_name |
|--------------|---------------|
| Laptop       | Shriya        |
| Laptop       | Sanjana       |
| Mouse        | Shriya        |
| Mouse        | Sanjana       |
| Keyboard     | Shriya        |
| Keyboard     | Sanjana       |

# g) NATURAL JOIN of Customers and Orders

| customer_name | order_id | order_date |
|---------------|----------|------------|
| Shriya        | 1        | 2024-10-01 |
| Shriya        | 2        | 2024-10-02 |
| Sanjana       | 3        | 2024-10-03 |

# h) Total Products Ordered by Each Customer (Join with Aggregation)

| customer_name | total_products_ordered |
|---------------|------------------------|
| Shriya        | 2                      |
| Sanjana       | 1                      |

# i) Multiple Joins Query

| customer_name | order_id | product_name | order_date |
|---------------|----------|--------------|------------|
| Shriya        | 1        | Laptop       | 2024-10-01 | 
| Shriya        | 2        | Mouse        | 2024-10-02 |
| Sanjana       | 3        | Keyboard     | 2024-10-03 |

## Employees Table

| employee_id | employee_name | department_id |
|-------------|---------------|---------------|
| 1           | Aarav         | 101           |
| 2           | Isha          | NULL          |
| 3           | Aditya        | 102           |
| 4           | Saanvi        | NULL          |

## Departments Table

| department_id | department_name |
|---------------|-----------------|
| 101           | HR              |
| 102           | IT              |
| 103           | Finance         |

## Full Outer Join

| Employee_name| department_name |
|--------------|-----------------|
| Aarav	       | HR              |
| Isha	       | NULL            |
| Aditya	   | IT              |
| Saanvi	   | NULL            |
| NULL	       | Finance         |

## Self Join

| Employee | Manager |
|----------|---------|
| Aarav	   | NULL    |
| Isha	   | Aarav   | 
| Aditya   | Aarav   |
| Saanvi   | Isha    |

## Join with Aggregration

| customer_name | total_products_ordered |
|---------------|------------------------|
| Aarav	        | 5                      |
| Isha	        | 3                      |
| Aditya	    | 2                      |

## FOREIGN KEYS:
# a)Foreign Key Definition
## Authors Table:

| author_id | author_name |
|-----------|-------------|
| 1	        | Vikram      |
| 2	        | Aishwarya   |

## Books Table:

| book_id |	book_title          | author_id |
|---------|---------------------|-----------|
| 1	      | Learn SQL           | 1         |
| 2	      | Mastering Databases | 2         |

# b)Cascading deletes
## Category Table:

| category_id |	category_name |
|-------------|---------------|
| 1	          | Electronics   |
| 2	          | Furniture     |

# c) Violating Forign Key Constraints

Error: FOREIGN KEY constraint failed





