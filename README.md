# SQL User Authentication System

This project implements a basic user authentication system with access logging capabilities. It includes scripts to create tables for storing user credentials and tracking user access.

## Database Setup

```sql
-- Create the database
CREATE DATABASE Practical15;
GO

-- Use the database
USE Practical15;
GO
```

## Table Structure

### Users Table

The Users table stores authentication credentials.

## 📌 Table: User

### **Insert Data For Task 1**
```sql

CREATE TABLE Users (
    Id INT IDENTITY(1,1) PRIMARY KEY,
    Username NVARCHAR(100) UNIQUE NOT NULL,
    FullName NVARCHAR(200) NOT NULL,
    Email NVARCHAR(200) NULL,
    Role NVARCHAR(50) NOT NULL
);
INSERT INTO Users (Username, FullName, Email, Role)
VALUES 
('Tejas22', 'Tejas', 'tejas@gmail.com', 'Admin'),
('Shivam21', 'Shivam', 'shivam@gmail.com', 'User');
```

### AccessLogs Table

The AccessLogs table tracks user login activity.

```sql
CREATE TABLE AccessLogs (
    Id INT PRIMARY KEY IDENTITY(1,1),
    UserName NVARCHAR(100),
    AccessTime DATETIME
);
```


### **Insert Data For Task 2**
```sql

CREATE TABLE FormUsers (
    Id INT IDENTITY(1,1) PRIMARY KEY,
    Username NVARCHAR(50) NOT NULL UNIQUE,
    Password NVARCHAR(255) NOT NULL
);
	
INSERT INTO FormUsers (Username, Password)
VALUES ('user1', '12345'),
		('user2','12345')

```

## Form Authentication
![image](https://github.com/user-attachments/assets/34f51f22-8a7f-48a0-b2fe-ec24c07c5b4e)

## Window Authentication
![image](https://github.com/user-attachments/assets/dfcfe4c9-c379-4a0c-ab0d-c4f1fd79a6d3)
![image](https://github.com/user-attachments/assets/3394248a-a358-4db4-b843-ccef99929567)



