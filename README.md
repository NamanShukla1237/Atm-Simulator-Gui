# ATM Simulator GUI - Java Project

A **single-file ATM Simulator GUI** project in Java that demonstrates core OOP concepts, multithreading, file handling, and optional database integration using JDBC. This project provides a simple ATM interface for depositing, withdrawing, checking balance, viewing mini statements, and more.

---

## Features

* **User Accounts**

  * Login with username and PIN.
  * Create new accounts with default balance `Rs10000`.
  * Change PIN functionality.

* **Account Operations**

  * Deposit and withdraw money.
  * Cheque deposit (processed in background using threads).
  * Mini statement showing last 5 transactions.
  * Export transaction history to a text file.
  * Simple interest calculator.

* **Database Integration (Optional)**

  * MySQL JDBC support to log transactions and update PIN.
  * If MySQL or driver not available, program continues with local memory.

* **GUI**

  * Swing-based GUI with clean layout and color-coded buttons.
  * Simple and user-friendly interface.

* **OOP Concepts**

  * Inheritance, polymorphism, interfaces, exception handling.
  * Multithreading for cheque deposits.
  * Collections usage: `Map` for accounts and PINs, `List` for mini statements.

## Prerequisites / Requirements

* **Java Development Kit (JDK)** 8 or higher installed.
* **IDE (optional):** Eclipse, IntelliJ IDEA, or any Java IDE.
* **MySQL database (optional):

  * JDBC URL, username, and password can be configured in `DatabaseManager` class.
  * Required only if you want to log transactions and persist user data.

## Setup & Run Instructions

### Using an IDE

1. Create a new Java project in your IDE.
2. Copy the `AtmSimulatorGui.java` file into the project.
3. Add MySQL JDBC driver to the project classpath if using database.
4. Run `AtmSimulatorGui.java` as a Java application.
5. The GUI will open for login and other operations.

### Using Command Line

1. Open terminal or command prompt.
2. Navigate to the folder containing `AtmSimulatorGui.java`.
3. Compile the program:
   javac AtmSimulatorGui.java
4. Run the program:
   java AtmSimulatorGui
 

### Optional MySQL Setup

* Create a database named `atm_db`.
* Create a table `users` with columns `username`, `pin`, `balance`.
* Update the JDBC URL, username, and password in the `DatabaseManager` class.
* If MySQL is not available, the program will use local memory to simulate accounts and transactions.

---

## Notes

* Default implementation is for a single user. You can expand it to multiple users.
* Modularizing the code into classes like `UserAccount`, `Transaction`, `DatabaseManager` is recommended for better structure.
* Ensure JDK is properly set in your environment for compilation and running.
