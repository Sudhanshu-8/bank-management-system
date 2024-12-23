# Bank Management System 💳

This is a banking application that simulates various banking operations such as account creation, deposits, withdrawals, balance inquiries, and PIN-based user authentication.

## Features

- **Account Creation:** Users can create a new account with their personal details.
- **Deposit & Withdrawals:** Deposit money into the account or withdraw funds securely.
- **Balance Inquiry:** Check the account balance at any time.
- **Transaction History:** View all past transactions for easy tracking.
- **Secure Login:** Users log in with a unique PIN for secure access.
- **MySQL Database Integration:** Data is stored and managed using MySQL for backend services.

## Get Started

### Prerequisites

- **Java Development Kit (JDK):** Ensure you have JDK 8 or later installed.
- **MySQL Database:** Make sure MySQL is installed and running.
- **MySQL JDBC Driver:** Ensure you have the MySQL JDBC driver configured.
- **A Java IDE:** Use IDEs like IntelliJ IDEA, Eclipse, or NetBeans.

### Steps to Run the App

1. **Clone the Repository**

   ```bash
   git clone https://github.com/sudhanshu-8/bank-management-system.git
   cd bank-management-system
   ```

2. **Set Up MySQL Database**

   - Create a database in MySQL called `bankmanagementsystem`.
   - Execute the necessary SQL scripts to set up the required tables.
   - Example SQL script:
   
     ```sql
     CREATE DATABASE bankmanagementsystem;
     USE bankmanagementsystem;
     CREATE TABLE login (pin VARCHAR(6), cardnumber VARCHAR(16), PRIMARY KEY(pin));
     CREATE TABLE bank (pin VARCHAR(6), type VARCHAR(50), amount INT, date DATETIME, FOREIGN KEY(pin) REFERENCES login(pin));
     ```

3. **Compile the Code**

   ```bash
   javac BankManagementSystem.java
   ```

4. **Run the Application**

   ```bash
   java BankManagementSystem
   ```

5. Enjoy managing banking transactions!

## How It Works

The Bank Management System allows users to perform various banking operations. Here's a breakdown of the main functionalities:

- **Account Creation:** Users can create an account by entering a unique PIN and card number.
- **Deposit and Withdraw Funds:** Users can deposit or withdraw money, with each action updating the database.
- **Transaction History:** Users can view a mini statement of their recent transactions.
- **Balance Inquiry:** Displays the current balance in the account.

## Project Structure

```
bank-management-system/
├── BankManagementSystem.java    # Main Java file
├── Conn.java                    # Database connection file
├── README.md                    # Project documentation
└── .gitignore                   # Git ignore file
```

## Learn More

- [MySQL JDBC Driver Documentation](https://dev.mysql.com/doc/connector-j/): Official documentation for MySQL JDBC driver.
- [Java 8 API Documentation](https://docs.oracle.com/javase/8/docs/api/): Learn about Java classes and methods.

## Want to Contribute?

Contributions are welcome! Fork the repository, make your changes, and submit a pull request. Whether it's a bug fix, new feature, or an improvement, we'd love to see your contributions.

Happy coding! ✨
