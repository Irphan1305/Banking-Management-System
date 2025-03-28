# Banking Management System

## Overview

The **Banking Management System** is a Java-based application designed to facilitate basic banking operations. It provides a user-friendly interface for managing customer accounts, processing transactions, and generating account statements.

## Features

- **Account Management**: Create, update.
- **Transactions**: Perform deposits.
- **Account Statements**: Generate and view detailed account statements for customers.

## Technologies Used

- **Programming Language**: Java
- **User Interface**: Java Swing
- **Database Management**: MySQL

## Prerequisites

Before running the application, ensure you have the following installed:

- Java Development Kit (JDK)
- MySQL Database Server
- An Integrated Development Environment (IDE) such as IntelliJ IDEA or Eclipse

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/Irphan1305/Banking-Management-System.git
```

### 2. Import the Project

- Open your IDE.
- Import the cloned project as a Java project.

### 3. Configure the Database

- Create a new MySQL database named `bankSystem`.
- Execute the following SQL commands to set up the required tables:

```sql
CREATE DATABASE bankSystem;
USE bankSystem;

CREATE TABLE signup (
    form_no VARCHAR(30), 
    name VARCHAR(30), 
    father_name VARCHAR(30), 
    DOB VARCHAR(30), 
    gender VARCHAR(30), 
    email VARCHAR(60), 
    marital_status VARCHAR(30), 
    address VARCHAR(60), 
    city VARCHAR(30), 
    pincode VARCHAR(30), 
    state VARCHAR(50)
);
SELECT * FROM signup;

CREATE TABLE signuptwo (
    form_no VARCHAR(30), 
    religion VARCHAR(30), 
    category VARCHAR(30), 
    income VARCHAR(30), 
    education VARCHAR(30), 
    occuption VARCHAR(60), 
    pan VARCHAR(30), 
    aadhar VARCHAR(60), 
    seniorcitizen VARCHAR(30), 
    existing_account VARCHAR(30)
);
SELECT * FROM signuptwo;

CREATE TABLE signupthree (
    form_no VARCHAR(30), 
    account_Type VARCHAR(40), 
    Card_number VARCHAR(30), 
    pin VARCHAR(30), 
    facility VARCHAR(200)
);
SELECT * FROM signupthree;

CREATE TABLE login (
    form_no VARCHAR(30), 
    Card_number VARCHAR(30), 
    pin VARCHAR(30)
);
SELECT * FROM login;

CREATE TABLE bank (
    pin VARCHAR(10), 
    date VARCHAR(50), 
    type VARCHAR(20), 
    amount VARCHAR(20)
);
SELECT * FROM bank;

SET SQL_SAFE_UPDATES = 0;
DELETE FROM login;
DELETE FROM bank;
DELETE FROM signup;
DELETE FROM signuptwo;
DELETE FROM signupthree;
```

- Update the database connection settings in the application to match your MySQL server configuration.

### 4. Build and Run the Application

- Compile the project using your IDE's build tools.
- Run the `Main` class to launch the application.

## Usage

### Admin Operations

- Create new customer accounts.
- Manage existing accounts.
- View all transactions and generate reports.

### Customer Operations

- Log in using account credentials.
- Perform deposits and withdrawals.
- Transfer funds to other accounts.
- View account balance and transaction history.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes with descriptive messages.
4. Push your changes to your fork.
5. Submit a pull request detailing your changes.

## License

This project is open-source and available under the [MIT License](LICENSE).

