# Elevate_Task7

Java JDBC – Employee Database App
📌 Overview

This is a simple Java console application that connects to a MySQL database and performs CRUD operations (Create, Read, Update, Delete) on an Employee table using JDBC.

🛠 Requirements

Java 8 or above

MySQL installed

MySQL Workbench (optional)

Maven (for dependencies)

MySQL JDBC Driver (mysql-connector-java)

📂 Database Setup

Open MySQL Workbench or terminal.

Run the following commands:

-- Create database
CREATE DATABASE employee_db;

-- Use database
USE employee_db;

-- Create table
CREATE TABLE employees (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    position VARCHAR(50),
    salary DECIMAL(10,2)
);

-- Insert sample data (optional)
INSERT INTO employees (name, position, salary) VALUES
('Alice Johnson', 'Manager', 75000.00),
('Bob Smith', 'Developer', 55000.00),
('Charlie Brown', 'Designer', 50000.00);

⚙️ Maven Dependency

Add this to your pom.xml:

<dependencies>
    <dependency>
        <groupId>mysql</groupId>
        <artifactId>mysql-connector-java</artifactId>
        <version>8.0.33</version>
    </dependency>
</dependencies>

▶️ How to Run

Clone or download the project.

Update database URL, username, password in EmployeeCRUD.java:

private static final String URL = "jdbc:mysql://localhost:3306/employee_db";
private static final String USER = "root";
private static final String PASSWORD = "your_password";


Compile and run:

mvn compile
mvn exec:java -Dexec.mainClass="EmployeeCRUD"

📌 Features

Add Employee

View Employees

Update Employee

Delete Employee
