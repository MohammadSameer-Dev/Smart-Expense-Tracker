
# 💰 Smart Expense Tracker

A simple desktop application built using **Python**, **Tkinter**, and **MySQL** that helps users record and view their daily expenses.
It allows you to **add**, **view**, and later extend to **delete or analyze** expenses.

This project demonstrates how to combine a **graphical user interface (GUI)** with a **database** using Python.

---

## 🧠 Project Overview

Managing money can be tricky, especially for students. This project provides a lightweight way to track daily spending.
Users can enter expenses with a **category**, **amount**, and **date**, and view them instantly in a table format.

The app can be improved to include monthly summaries, charts, and export options — but the current version focuses on core database functionality and Tkinter integration.

---

## 🧩 Features

✅ Add new expense entries (category, amount, date)
✅ View all saved expenses in a table
✅ Simple and interactive Tkinter GUI
✅ Data stored permanently in MySQL database
✅ Easy to set up and understand for beginners

---

## 🏗️ Technologies Used

| Component            | Technology Used            | Purpose                                   |
| -------------------- | -------------------------- | ----------------------------------------- |
| Programming Language | **Python 3**               | Core logic                                |
| GUI Library          | **Tkinter**                | Interface for adding and viewing expenses |
| Database             | **MySQL**                  | Stores expense records                    |
| Library              | **mysql-connector-python** | Connects Python with MySQL                |

---

## 📂 Project Structure

```
SmartExpenseTracker/
├── main.py             # Entry point - runs the app
├── gui.py              # Tkinter GUI design
├── db.py               # Database connection and functions
├── config.py           # MySQL connection settings
├── schema.sql          # SQL script to create the database and table
├── requirements.txt    # Required Python packages
└── README.md           # Project documentation (this file)
```

---

## ⚙️ Installation & Setup

### 1. Install Python

Download and install **Python 3.x** from [python.org/downloads](https://www.python.org/downloads/).
Make sure to check **“Add Python to PATH”** during installation.

### 2. Install MySQL

Install **MySQL Server** (for Windows, you can use [MySQL Installer](https://dev.mysql.com/downloads/installer/)).
Note down your MySQL **username**, **password**, and **port**.

### 3. Create the Database

Open MySQL Command Line or Workbench, and run the script below or open `schema.sql` file:

```sql
CREATE DATABASE IF NOT EXISTS expense_tracker;
USE expense_tracker;

CREATE TABLE IF NOT EXISTS expenses (
    id INT AUTO_INCREMENT PRIMARY KEY,
    category VARCHAR(50),
    amount DECIMAL(10,2),
    date DATE
);
```

### 4. Configure Database Connection

Edit **config.py** with your own MySQL details:

```python
DB_HOST = "localhost"
DB_USER = "root"
DB_PASS = ""           # your MySQL password
DB_NAME = "expense_tracker"
```

### 5. Install Dependencies

Open your terminal or command prompt inside the project folder and run:

```bash
pip install -r requirements.txt
```

*(If you get any error about “tkinter”, it’s usually already built into Python — no need to install separately.)*

### 6. Run the Application

Run this command to start:

```bash
python main.py
```

---

## 🖥️ How It Works

1. When the app starts, it opens a **Tkinter window** titled “Smart Expense Tracker.”
2. You can enter a **Category**, **Amount**, and **Date (YYYY-MM-DD)**.
3. Click the **Add Expense** button — the record is saved into the MySQL database.
4. All stored expenses automatically appear in the table below.

---

## 📸 Example Interface (Conceptual)

```
+--------------------------------------+
|          Smart Expense Tracker       |
+--------------------------------------+
| Category: [___________]              |
| Amount:   [___________]              |
| Date:     [YYYY-MM-DD]               |
| [Add Expense]                        |
----------------------------------------
| ID | Category | Amount | Date        |
|----|-----------|--------|------------|
| 1  | Food      | 120.00 | 2025-10-28 |
| 2  | Travel    | 75.00  | 2025-10-27 |
----------------------------------------
```

---

## 🧱 Files Explained

| File                 | Description                                                  |
| -------------------- | ------------------------------------------------------------ |
| **main.py**          | The starting point that calls the Tkinter GUI.               |
| **gui.py**           | Contains the design for the window, input fields, and table. |
| **db.py**            | Handles saving and retrieving data from MySQL.               |
| **config.py**        | Stores MySQL login details and database name.                |
| **schema.sql**       | SQL commands to create your database and table.              |
| **requirements.txt** | List of required Python libraries.                           |

---

## 💡 Future Improvements

If you want to take this project further, you can add:

* Delete and update buttons for expenses.
* Pie chart for monthly spending summary (using `matplotlib`).
* CSV or Excel export feature.
* Login system for multiple users.

---

## 🧑‍💻 Example Output in Console

When adding expenses, the database table will look like this:

| id | category | amount | date       |
| -- | -------- | ------ | ---------- |
| 1  | Food     | 120.00 | 2025-10-28 |
| 2  | Travel   | 75.00  | 2025-10-27 |

---

## 🧾 License

This project is made for **educational purposes** and is free to use, modify, and share.

---
