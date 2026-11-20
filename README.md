# smart-expense-ledger
A Java-based expense management system to track daily expenses, manage budgets, and monitor personal finances.
# SmartExpense & Split Ledger

## Overview
SmartExpense & Split Ledger is a Java console application that helps individuals and small groups track daily expenses, categorize spending, calculate shared balances, and generate summary reports. It solves the problem of scattered expense notes and manual splitting calculations by storing structured records persistently in a relational database with clear validation and clean object-oriented design.

## Technologies Used
- **Java** (Java 17+)
- **Object-Oriented Programming (OOP)** (Encapsulation, Inheritance/Polymorphism via interfaces, Custom Exceptions, Layered Architecture)
- **SQL** (MySQL / PostgreSQL / SQLite with JDBC)
- **Other Technologies Used** (Maven, Git)

## Features
- **Expense & Category Management:** Add, view, filter, and delete expenses across categories (e.g., Food, Travel, Utilities, Rent) with input validation.
- **Shared Expense Splitting:** Split bills equally or by custom amounts/shares among group members and compute net balances.
- **Spending & Balance Reports:** View total spend by category or date range and see who owes whom at a glance.

## Project Structure
```text
smart-expense-ledger/
├── src/
│   ├── main/
│   │   ├── java/com/smartexpense/
│   │   │   ├── Main.java                 # Application entry point & menu loop
│   │   │   ├── model/                    # Expense, Member, SplitEntry, Category
│   │   │   ├── service/                  # Business logic & balance calculation rules
│   │   │   ├── repository/               # JDBC database access & SQL queries
│   │   │   ├── exception/                # Custom domain exceptions (e.g., InvalidAmountException)
│   │   │   └── util/                     # Input readers, formatters, DB connection helper
│   │   └── resources/
│   │       ├── db.properties.example     # Sample DB configuration template
│   │       └── schema.sql                # SQL tables for users, expenses, and splits
│   └── test/                             # Unit tests (optional / future)
├── pom.xml                               # Maven dependencies (JDBC driver, etc.)
└── README.md
