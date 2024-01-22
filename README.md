# SQLPracticeQuestions
Just a practice test / question set with answers and an explanation


The terms “bitmap, “b-tree”, and “hash” refer to which type of database structure?

A. View
B. Function
C. Index
D. Stored Procedure
E. Trigger

Answer: C. Index
Explanation: A bitmap is an array of bits, a b-tree is a sorted data structure, and a hash is a data structure that stores data in key-value pairs. These are all types of indices, therefore the answer is C. Index.

—------------------------------------------

One reason to add an index is to:

A. Decrease storage space.
B. Increase database security.
C. Improve performance of select statements.
D. Improve performance of insert statements.


Answer: C. Improve performance of select statements.
Explanation: An index allows for sorted data, instead of just randomly scrambled. By indexing your select statement, you're able to get results quicker as you don’t have to start at the first row.

—------------------------------------------

You have a table that contains the following data.

You break the table into the following two tables.

This process is referred to as;

A. defragmentation
B. normalization
C. fragmentation
D. denormalization

Answer: B. normalization
Explanation: Normalization is the process of breaking a table into separate tables to reduce the amount of reused data. More information on normalization can be found here.

—------------------------------------------

Which statement creates a composite key?


A. Option A
B. Option B
C. Option C
D. Option D

Answer: D. Option D
Explanation: A composite key is the combination of two columns, so OrderID and OrderItemID in this case, which allows multiple columns to be uniquely identified. Source

—------------------------------------------

Which command should you use to give a user permission to read the data in a table?
A. ALLOW SELECT
B. LET READ
C. PERMIT READ
D. GRANT SELECT

Answer: D. GRANT SELECT
Explanation: GRANT is the keyword that is used for most SQLs for giving a user specific permissions. SELECT is the permission that allows a user to read data. Therefore the answer is D.

—------------------------------------------

You need to enable a new employee to authenticate to your database. Which command should you use?

A. ALLOW USER
B. CREATE USER
C. ADD USER
D. INSERT USER
E. ALTER USER

Answer: B. CREATE USER
Explanation: Not much to explain, CREATE USER is the only one of these that creates a new user.

—------------------------------------------

Which keyword can be used in a create table statement?

A. ORDER BY
B. DISTINCT
C. GROUP BY
D. UNIQUE

Answer: D
Explanation: The only one of these options that can be used while creating a table is UNIQUE. While creating a table you can’t order the data, as there is no data yet. You can’t use DISTINCT as you're not gathering data in a create table statement. Finally you can’t group the data, as there is still no data.

—------------------------------------------

You need to store product quantities, and you want to minimize the amount of storage space that is used. Which data type should you use?

A. INTEGER
B. DOUBLE
C. COUNT
D. FLOAT

Answer: A. INTEGER
Explanation: A double and float data type use more storage space, as they take decimals into account. The INTEGER will be less accurate, but that is not important for this question. And COUNT isn't a data type.

—------------------------------------------

You have the following table definition:

CREATE TABLE Road 
	(RoadID INTEGER NOT NULL,
	Distance INTEGER NOT NULL)

The Road table contains the following data:

You execute the following statement:
INSERT INTO Road VALUES (1234, 36)

What is the result?

A. An error stating that NULL values are not allowed.
B. A new row in the table.
C. An error stating that duplicate IDs are not allowed.
D. A syntax error.

Answer: B
Explanation: No errors will arise, as no NULL data is passed since the INSERT fills all columns in the table. The CREATE TABLE statement shows that none of the rows can’t have duplicate data. And the INSERT statement has correct syntax. Therefore a new row will be created.

—------------------------------------------

One reason to create a stored procedure is to:

A. Improve performance
B. Minimize storage space.
C. Bypass case sensitivity requirements.
D. Give the user control of the query logic.

Answer: A. Improve performance
Explanation: A stored procedure is similar to a user created function. It increases performance since the query plans get cached. Which is bad for minimizing storage space, however that is irrelevant for this question. Source

—------------------------------------------

Which permission does a user need in order to run a stored procedure?

A. EXECUTE
B. ALLOW
C. CALL
D. RUN

Answer: A. EXECUTE
Explanation: EXECUTE is the name of the permission that needs to be granted to a user to allow them to use stored procedures, which can then be run with the keyword EXEC.

—------------------------------------------

In SQL, an insert statement is used to add a:

A. User to a database
B. Row of data to a table.
C. Table to a database.
D. Column to a table definition.

Answer: B
Explanation: INSERT is used to insert new data into an already created table. Source

—------------------------------------------

You have two tables. Each table has three rows. 

How many rows will be included in the Cartesian product of these two tables?

A. 0
B. 3
C. 6
D. 9

Answer: D
Explanation: A Cartesian is a type of JOIN, also known as a CROSS JOIN. Which usually results in the amount of rows equal to the rows in tableA * the rows in tableB. I recommended reading more about cross/cartesian joins here

—------------------------------------------

You are writing an SQL statement to retrieve rows from a table.

Which data manipulation language (DML) command should you use?

A. READ
B. SELECT
C. OUTPUT
D. GET

Answer: B
Explanation: SELECT is used to retrieve data from specific tables. It can also be specified to gather data from specific rows. Source

—------------------------------------------

Which constraint ensures a unique value in the ID column for each customer?

A. DISTINCT
B. FOREIGN KEY
C. SEQUENTIAL
D. PRIMARY KEY

Answer: D
Explanation: DISTINCT may seem like the obvious choice at first glance, however the DISTINCT keyword is used while getting data and is NOT a constraint. A primary key ensures that each value for the specific column will be different from each other. 

—------------------------------------------

You have the following table definition:

CREATE TABLE Product
(ID INTEGER PRIMARY KEY,
Name VARCHAR(20),
Quantity INTEGER)

The Product table contains the following data.

You execute the following statement:
SELECT Name FROM Product WHERE Quantity IS NOT NULL

How many rows are returned?

A. 0
B. 1
C. 2
D. 3
E. 4

Answer: D
Explanation: IS NOT NULL means that the data in the row exists, i.e != NULL. The select statement is gathering names, but we don’t really care about what is gathered, only how much is gathered. The WHERE is a condition, so if the condition is true in the statement, it will return the name of the product. Since the quantity for Plums in the Product table is nonexistent, it is NULL, while all the other products have data in the quantity column, so the total number of returned rows are 3.

—------------------------------------------

You are writing a select statement to find every product whose name contains a specific character. Which keyword should you use in your where clause?

A. FIND
B. BETWEEN
C. INCLUDES
D. LIKE

Answer: D. LIKE
Explanation: LIKE is frequently used in a WHERE statement, and WHERE is checking for a specific condition. So if you want to find all products that start with the letter ‘b’ you can do
SELECT ProductName
FROM Products
WHERE ProductName LIKE ‘b%’
For more information on LIKE check here
I also recommend learning the wildcards which can be found here
—------------------------------------------

A database contains two tables named Customer and Order.

You execute the following statement:

DELETE FROM Order
WHERE CustomerID = 209

What is the result?

A. The first order for CustomerID 209 is deleted from the Order table.
B. All orders for the CustomerID 209 are deleted from the Order table, and CustomerID 209 is deleted from the Customer table.
C. All orders for CustomerID 209 are deleted from the Order table.
D CustomerId 209 is deleted from the Customer table.

Answer: C
Explanation: The first line specifies that we are removing data and only from the Order table. The WHERE statement is specifying the condition. So WHERE the CustomerID is 209, it will be deleted from inside the Order table.

—------------------------------------------

You have a table named product. The Product table has columns for ProductDescription and ProductCategory. You need to change the ProductCategory value for all the spoons in the Product table to 43.
Which statement should you use?

A. Option A.
B. Option B.
C. Option C.
D. Option D.

Answer: A
Explanation: Answer A correctly changes the ProductCategory to 43 for ALL ProductDescriptions with ‘spoon’. First it specifies that the command will update the table, then it shows what command is going to take place, after the condition (WHERE) is found.

—------------------------------------------

You have a table that contains information about all students in your school. 
Which SQL keyword should you use to change a student’s first name in the table?

A. UPDATE
B. CHANGE
C. SELECT
D. INSERT

Answer: A
Explanation: UPDATE is the keyword that specifies that you’re changing information in a table. For an example check the question above.

—------------------------------------------

You need to populate a table named EmployeeCopy with data from an existing table named Employee. Which statement should you use?

A. Option A
B. Option B
C. Option C
D. Option D

Answer: D
Explanation: D is the most  correct for this example, however it may be different on the test. When using an INSERT INTO, you should specify the columns that will be filled, and the values in the SELECT statement. This example assumes that all the data will fit into the columns inside EmployeeCopy from Employee without error.

—------------------------------------------

You execute the following statement:
SELECT DepartmentName
	FROM Department
	WHERE DepartmentID = 
		(SELECT DepartmentID
		FROM Employee
		WHERE EmployeeID = 1234)

This statement is an example of a/an:

A. Subquery
B. Union
C. Outer join
D. Cartesian product

Answer: A. Subquery
Explanation: A subquery is similar to a nested loop in other programming languages. The statement above is an example of one. More information can be found on subqueries here

—------------------------------------------

Which keyword would you use in a select statement to return rows that meet a specific condition?

A. WHERE
B. UNION
C. ORDER BY
D. FROM

Answer: A. WHERE
Explanation: WHERE is a condition statement, meaning that if the condition that is specified in the WHERE statement is met, the statements relying on it will be ran. More information can be found here.

—------------------------------------------

Which category of SQL statements is used to add, remove, and modify database structures?

A. Data access language. (DAL)
B. Data manipulation language. (DML)
C. Data control language. (DCL)
D. Data definition language. (DDL)

Answer: D. Data definition language. (DDL)
Explanation: DDL, or data definition language, is the name for the syntax that is used for creating and modifying database objects, such as tables and users.

—------------------------------------------

You have a Customer table and an Order table. You join the Customer table with the Order table by using the CustomerID column.

The Results include:
-All customers and their orders
-Customers who have no orders

Which type of join do these results represent?

A. Complete join
B. Partial join
C. Inner join
D. Outer join

Answer: D. Outer join
Explanation: The results show that all data from both tables is brought together, that shows us that it's an Outer join, more specifically a FULL OUTER JOIN.

—------------------------------------------

Data in a database is stored in:

A. Tables
B. Queries.
C. Data types.
D. Stored procedures.

Answer: A. Tables
Explanation: Queries hold statements that are executed to modify/change/update/remove/ect. Data types are like a string, integer, or similar. A stored procedure is a query that is stored and cached inside the database that can be run with better performance than just running it by itself multiple times, however it does not hold data itself. Tables DO hold data, they are organized by column and rows, rows being the data that is inserted and columns being the keys that show what the data is.

—------------------------------------------

You have a table named Student that contains 100 rows. Some of the rows have a NULL value in the FirstName column.

You execute the following statement:

DELETE FROM Student

What is the result?

A. All rows in the table will be deleted.
B. All rows containing a NULL value in the FirstName column will be deleted.
C. You will receive an error message.
D. All rows and table definitions will be deleted.

Answer: A. All rows in the table will be deleted
Explanation: The statement doesn’t specify what data will be deleted, it only says to delete the data found inside the Student table. Therefore all rows in the table will be deleted.

—------------------------------------------

Which database term is used to describe the process of applying a backup to a damaged or corrupt database?

A. Recover
B. Restore
C. Commit
D. Attach

Answer: B
Explanation: The RESTORE term is used to restore data from a backup. More information on RESTORE can be found here.

—------------------------------------------
You have a table named Product that contains one million rows.

You need to search for product information in the Product table by using the product’s unique ID.
What will make this type of search more efficient?

A. A cursor
B. A subquery
C. A trigger
D. An index

Answer: D. An index
Explanation: An index allows you to quickly parse data inside a database. You can add one using the statement:
CREATE INDEX index_name
ON table_name (column1, column2, …);
However the data for the specific column cannot be found in another row of the same column.

—------------------------------------------

One difference between a function and a stored procedure is that a function:

A. Must be called from a trigger.
B. Must return a value.
C. Cannot contain a transaction.
D. Cannot accept parameters. 

Answer: B. Must return a value.
Explanation: A function returns a value, such as when you use the MAX() function, the max of the passed data is returned, which is required of the function, otherwise you’ll get an error. A stored procedure does not need to return a value.

—------------------------------------------

Which keyword must be included in a create view statement?

A. WHERE 
B. ORDER BY
C. UPDATE
D. SELECT

Answer: D. SELECT
Explanation: While creating a view, there is nothing to order or update, so it can’t be either of those. A SELECT is needed so that you can specify what data is going to be used inside of the view. More information can be found here.
—------------------------------------------

You need to remove a view named EmployeeView from your database. Which statement should you use?

A. DELETE VIEW EmployeeView
B. DELETE EmployeeView
C. DROP EmployeeView
D. DROP VIEW EmployeeView

Answer: D. DROP VIEW EmployeeView
Explanation: We use DROP to specify removing as DELETE is for rows and data inside of the database. Then we specify that we are dropping a VIEW, a view that is named EmployeeView.

—------------------------------------------

A view can be used to:

A. Save an extra copy of data stored in a separate table.
B. Limit access to specific rows or columns of data in a table.
C. Ensure referential integrity
D. Save historical data before deleting it from the base table.

Answer: B
Explanation: A VIEW is used to have a copy of a specific part of the data. It can be entire databases, to specific rows.

—------------------------------------------

On which database structure does an update statement operate?

A. Table
B. User
C. Trigger
D. Role

Answer: A. Table
Explanation: An UPDATE statement can only be applied to a table. 

—------------------------------------------

You need to list the name and price of each product, sorted by price from highest to lowest. Which statement should you use?

A. Option A.
B. Option B.
C. Option C.
D. Option D

Answer: A. Option A
Answer: To start, we need the Name and Price data, so we do:
SELECT Name, Price
Then we need to specify the location of the data, which would be:
FROM Product
And finally we need to order the data from highest to lowest price.
ORDER BY Price DESC
DESC specifies that we start at the highest value, then go down, and it bases it off the Price data.

—------------------------------------------

You delete rows in a table named Order. The corresponding rows in the Orderitem table are automatically deleted. 
This process is a/an example of:

A. Inherited Delete
B. Cascade Delete
C. Functional Delete
D. Waterfall Delete
E. Domino Delete

Answer: B. Cascade Delete
Explanation: Cascade Deletes occur when data can no longer be associated with its “parent”, mainly due to the parent data being deleted. 

—------------------------------------------

Which statement deletes the rows where the employee’s phone number is not entered?

Option A
Option B
Option C
Option D

Answer: A. Option A
Explanation: The answer isn’t B, since that would delete all rows where data IS NOT NULL.
It’s not C, since the wildcard character “%” is also for any data, so it would delete any NOT NULL data, basically the same as B. Finally it’s not D, since NULLABLE would look for rows that can be NULL.

—------------------------------------------

Which two elements are required to define a column? (Choose two.)

A. A name
B. A key
C. An index
D. A data type

Answer: A, D
Explanation: To define a column,  you must give it a name, to describe what will be stored in that column, and a data type to specify what is being stored.

—------------------------------------------

What defines the amount of storage space that is allocated to a value in a column?

A. Format
B. key
C. Data type
D. Validator

Answer: C. Data type
Explanation: Different data types require different amounts of storage, for example a float takes more storage space than an integer, since it has to accommodate for the decimal value.

—------------------------------------------

You have a Department table and an Employee table in your database.

You need to ensure that an employee can be assigned to only an existing department.

What should you apply to the Employee table?

A. A primary key
B. An index
C. A foreign key
D. A unique constraint
E. A data type

Answer: C. A foreign key
Explanation: A FOREIGN KEY would be used for this. Since a foreign key refers to the PRIMARY KEY of another table, and a PRIMARY KEY has to have a unique value for each instance of the row, it would mean that only one employee can be assigned to a specific department. 

—------------------------------------------

What are three valid data manipulation language (DML) commands? (Choose three.)

A. INSERT
B. COMMIT
C. DELETE
D. OUTPUT
E. UPDATE

Answer: A, C, E
Explanation: COMMIT and OUTPUT don’t manipulate data, however the rest do.

—------------------------------------------

Which type of index changes the order in which the data is stored in a table?


A. Non-sequential
B. Sequential
C. Non-clustered
D. Clustered

Answer: D. Clustered
Explanation: A clustered index determines the physical order of the data in a table based on the indexed column. When a table has a clustered index, the rows are stored on disk in the same order as the index. This means that the data is physically organized on disk. Compared to the other indexes that creates a separate structure.

—------------------------------------------

You have a table that contains product IDs and product names.

You need to write an UPDATE statement to change the name of a specific product to glass.

What should you include in the update statement?

A. SET ProductName = ‘glass’
B. LET ProductName = ‘glass’
C. EXEC ProductName = ‘glass’
D. ASSIGN ProductName = ‘glass’

Answer: A. SET ProductName = ‘glass’
Explanation: When creating an UPDATE statement, you want to use the SET keyword. More information on UPDATE/SET can be found here.


—------------------------------------------

On which database structure does an insert statement operate?

A. Role
B. Trigger
C. User
D. Stored Procedure
E. Table

Answer. E. Table
Explanation: You use insert to insert data into a table. An insert cannot be used on any of the other options.

—------------------------------------------

You have a table of products with fields for ProductID, Name, and Price.

You need to write an UPDATE statement that sets the value in the InStock field to Yes for a specific ProductID.

Which clause should you use in your update statement?

A. THAT
B. WHERE
C. GROUP BY
D. HAVING

Answer: B. WHERE
Explanation: WHERE is the clause for the UPDATE statement that specifies what will be updated. Since we want only products that are in stock, we will specify that in the WHERE.

—------------------------------------------

You have the database table named Cars as defined below:

You have the following Structured Query Language (SQL) statement:

How many rows are returned by the SQL statement?

A. 4
B. 5
C. 6
D. 7

Answer: A. 4
Explanation: The <> operator means not equal, similar to !=. So its searching the table Cars that don’t have a USA origin or are the color Black.

—------------------------------------------

You accept an IT internship at a local charity. The charity asks you to keep a record of its volunteers by using a database.

The table has the following columns and rows:

When volunteer information changes, you must update the table. 

You need to change Tia’s name to Kimberly.
Which statement should you choose?

A. Option A
B. Option B
C. Option C
D. Option D

Answer: D. Option D
Explanation: The answer must start with UPDATE to specify that we are updating an existing table. So it can’t be A or B. And it can’t be C, since the syntax on UPDATE is incorrect. When using an UPDATE statement, you put the table that is being updated after the UPDATE, not what you want to change.

—------------------------------------------

This question requires that you evaluate the underlined text to determine if it is correct.

Use the FROM keyword in a SELECT statement to return rows that meet a specific condition.

Instructions: Review the underlined text. If it makes the statement correct, select “No change is needed.” If the statement is incorrect, select the answer choice that makes the statement correct.

A. No change is needed.
B. ORDER BY
C. UNION
D. WHERE

Answer: D. WHERE
Explanation: The FROM specifies the table that is being selected, you need a WHERE to specify the condition on what will change.

—------------------------------------------




