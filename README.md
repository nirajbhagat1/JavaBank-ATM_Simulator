JavaBank - ATM Simulator
JavaBank is a simulation of an ATM system developed in Java, using Swing for the user interface and MySQL for data management. The project features both an admin and user module to facilitate secure account management, transaction processing, and banking operations in a realistic setting.

Table of Contents
Project Overview
Features
Technologies Used
Database Setup
Installation & Setup
Usage
Project Structure
Screenshots
License
Project Overview
JavaBank is designed to mimic the core functionalities of a real-world ATM system, offering secure login, user account operations, and transaction management. The project structure includes tables to store user information, account details, and transaction history.

Features
Admin Module
Secure Login: Admins can log in securely to manage user accounts.
Account Management: Create, update, and delete user accounts.
Transaction Monitoring: View all user transactions.
User Module
Secure Login with PIN: Users can access their accounts with a PIN.
Account Operations: Functions include account creation, funds transfer, deposit, and withdrawal.
Transaction History: Users can view transaction history for recent activities.
Technologies Used
Java (Swing & AWT): For the GUI and business logic.
MySQL: To manage data for users, accounts, and transactions.
Database Setup
The database schema includes multiple tables to store user details, account information, and transactions.

Create Database and Tables

sql
Copy code
CREATE DATABASE bankmanagementsystem;
USE bankmanagementsystem;

-- User signup information
CREATE TABLE signup (
  formno VARCHAR(20),
  name VARCHAR(20),
  father_name VARCHAR(20),
  dob VARCHAR(20),
  gender VARCHAR(20),
  email VARCHAR(30),
  marital_status VARCHAR(20),
  address VARCHAR(40),
  city VARCHAR(25),
  pincode VARCHAR(20),
  state VARCHAR(25)
);

-- Additional user information
CREATE TABLE signup2 (
  formno VARCHAR(20),
  religion VARCHAR(20),
  category VARCHAR(20),
  income VARCHAR(20),
  education VARCHAR(20),
  occupation VARCHAR(20),
  pan VARCHAR(20),
  aadhar VARCHAR(20),
  seniorcitizen VARCHAR(20),
  existingaccount VARCHAR(20)
);

-- Account information
CREATE TABLE signup3 (
  formno VARCHAR(20),
  accountType VARCHAR(40),
  cardno VARCHAR(25),
  pin VARCHAR(10),
  facility VARCHAR(100)
);

-- Login information
CREATE TABLE login (
  formno VARCHAR(20),
  cardno VARCHAR(25),
  pin VARCHAR(10)
);

-- Transactions
CREATE TABLE bank (
  pin VARCHAR(10),
  date VARCHAR(50),
  mode VARCHAR(20),
  amount VARCHAR(20)
);
Use TRUNCATE statements to reset tables as needed:

sql
Copy code
TRUNCATE TABLE login;
TRUNCATE TABLE signup;
TRUNCATE TABLE signup2;
TRUNCATE TABLE signup3;
TRUNCATE TABLE bank;
Installation & Setup
Prerequisites
Java JDK 8 or later
MySQL
Steps
Clone the Repository

bash
Copy code
git clone https://github.com/your-username/JavaBank-ATM-Simulator.git
cd JavaBank-ATM-Simulator
Database Configuration

Set up the database as per the instructions in the Database Setup section.
Update Conn.java with your MySQL credentials:
java
Copy code
Class.forName("com.mysql.jdbc.Driver");
this.c = DriverManager.getConnection("jdbc:mysql:///bankmanagementsystem", "your_username", "your_password");
Run the Application

Open the project in an IDE, build, and run JavaBankMain.java.
Usage
Admin Access

Log in as an admin to manage user accounts and monitor transactions.
User Access

Log in with a PIN to access account options such as deposit, withdrawal, funds transfer, and transaction history.
Project Structure
css
Copy code
JavaBank-ATM-Simulator/
├── src/
│   ├── ASimulatorSystem/
│   │   ├── Conn.java
│   │   ├── JavaBankMain.java
│   ├── admin/
│   ├── user/
│   ├── db/
├── database/
│   └── bankmanagementsystem.sql
├── README.md
└── LICENSE
Screenshots
(Include screenshots of login screens, admin panel, and user transaction pages to illustrate functionality)
