Java JDBC Employee Database Application
This project demonstrates fundamental CRUD (Create, Read, Update, Delete) operations using Java Database Connectivity (JDBC) to interact with a relational database (MySQL or PostgreSQL).

Objectives
1)Establish a secure connection to a MySQL/PostgreSQL database using the appropriate JDBC driver.

2)Implement standard database operations using Connection, PreparedStatement, and ResultSet.

3)Provide a simple console-based interface for managing employee records.

Prerequisites
. Java Development Kit (JDK): Version 11 or higher.

. Database Server: A running instance of MySQL or PostgreSQL.

. JDBC Driver JAR: You need to download and include the correct JDBC driver JAR file (e.g., mysql-connector-java.jar or postgresql-42.x.x.jar) in your project's classpath.

VS Code: (Or any preferred IDE) configured to run Java projects with external libraries.

Setup Instructions
1. Database Setup
Execute the SQL script provided in the database_setup.sql file to create the necessary database and table.

Example Commands (in your database client):

-- Create the database
CREATE DATABASE employee_db;

-- Use the database
\c employee_db -- for PostgreSQL
USE employee_db; -- for MySQL

-- Run the table creation script
-- (See database_setup.sql content below)

2. Project Configuration (Java)
. Place the EmployeeDatabaseApp.java file in your Java project source folder.

. Update Connection Details: Open EmployeeDatabaseApp.java and modify the following constants with your database credentials:

DB_URL

DB_USER

DB_PASSWORD

Update Driver: Ensure the JDBC_DRIVER constant is set correctly for your database:

MySQL: com.mysql.cj.jdbc.Driver

PostgreSQL: org.postgresql.Driver

Add Driver to Classpath: Configure your IDE (VS Code, IntelliJ, etc.) to include the downloaded JDBC driver JAR file in the project's build path/classpath.

Running the Application
Compile and run EmployeeDatabaseApp.java.

The application will present a console menu:

--- Employee Database Management ---
1. Add New Employee
2. View All Employees
3. Update Employee Salary
4. Delete Employee
5. Exit
Enter your choice:

Enter the number corresponding to the desired operation.

Key JDBC Components Used
Component

. Purpose

. Connection

. Manages the physical connection session between the Java application and the database.

PreparedStatement

. Used for executing pre-compiled SQL statements, which is crucial for security (prevents SQL Injection) and performance.

. ResultSet

. Represents the result set of a database query, providing methods to iterate over rows and retrieve column data.

try-with-resources

Ensures that all JDBC resources (Connection, Statement, ResultSet) are automatically closed, preventing resource leaks.
