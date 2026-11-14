# Employee Management System

A Desktop GUI application built with **Python (Tkinter)** and **MySQL (PyMySQL)** to manage employee records, calculate salaries, update details, and manage database persistence.

---

## 📌 Features

* **Add Employee Details:** Store Employee ID, Name, Mobile Number, Department, and Salary.
* **View Records:** Display all recorded employees in a structured `Treeview` table.
* **Salary Portal:** Dedicated window to fetch and check salary details by Employee ID.
* **Update Records:** Fetch specific records by ID and modify existing details.
* **Delete Records:** Remove employee records easily using their unique ID.
* **Clear Table:** Wipe the current treeview display with a single click.

---

## 🛠️ Tech Stack & Requirements

* **Language:** Python 3.x
* **GUI Library:** Tkinter (built-in with Python)
* **Database:** MySQL Server
* **Database Connector:** `pymysql`

---

## 🚀 Getting Started

Follow these instructions to clone the repository and set up the project on your local machine.

### 1. Prerequisites

Make sure you have Python and MySQL Server installed on your machine:
* [Download Python](https://www.python.org/downloads/)
* [Download MySQL Server](https://dev.mysql.com/downloads/mysql/)

### 2. Clone the Repository

Open your terminal or command prompt and run:

```bash
git clone https://github.com/chetanpadwal2310/Employee-Management-System.git
cd Employee-Management-System
```

---

## ⚙️ Installation & Setup

### Step 1: Install Dependencies

Install `PyMySQL` via pip:

```bash
pip install pymysql
```

### Step 2: Database Configuration

Before running the application, update the MySQL configuration settings in the Python script (`localhost`, `username`, `password`, and `port`) to match your local MySQL setup:

```python
# Change user, password, and port to match your local MySQL installation
conn = pymysql.connect(
    user='root',
    host='localhost',
    password='YOUR_MYSQL_PASSWORD',
    port=3306  # Standard MySQL port (or 3307 if customized)
)
```

### Step 3: Initialize Database & Tables

Run the database setup code blocks inside the Jupyter Notebook or Python script to create the required database and table structure:

```sql
-- Database: emp_db
CREATE DATABASE emp_db;

-- Table: emp
CREATE TABLE emp (
    emp_id VARCHAR(10) PRIMARY KEY,
    emp_name VARCHAR(100),
    mob_no VARCHAR(15),
    dept VARCHAR(50),
    emp_salary VARCHAR(20)
);
```

---

## 💻 Running the Application

If using Jupyter Notebook:
1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Open the main notebook file.
3. Run all cells sequentially.

If converted to a standard Python script (`.py`):
```bash
python main.py
```

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).