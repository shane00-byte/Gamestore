# Gamestore

---

# 🎮 Gaming Store Database Manager

A **Python + MySQL** command-line application to manage records for a gaming store. It allows you to insert, update, delete, and display entries related to **games** and **consoles** in a MySQL database.

## 📌 Features

- 🎯 Manage **game records** (`gamestore` table)
  - Add new games
  - Update existing game details
  - Delete games
  - View all games

- 🕹️ Manage **console records** (`console` table)
  - Add new consoles
  - Update existing console details
  - Delete consoles
  - View all consoles

## 🧰 Requirements

- Python 3.x
- MySQL server (with a database named `game`)
- Tables:
  - `gamestore(product_id, product_name, company, type, category, price)`
  - `console(product_id, product_name, features, colours, company, price)`
- Python MySQL connector:
  
```bash
pip install mysql-connector-python
```

## 🚀 How to Run

1. **Ensure MySQL is running** and the database `game` with tables `gamestore` and `console` exists.
2. **Update MySQL credentials** in the script if necessary:

```python
mysql.connect(
    host="localhost",
    user="root",
    port="3306",
    password="1234",
    database="game"
)
```

3. **Run the script**:

```bash
python game_store_manager.py
```

## 🧾 Menu Example

```
WHAT DO YOU WANT TO EXPLORE TODAY?
ENTER G FOR GAMES
ENTER C FOR CONSOLES
ENTER YOUR CHOICE: G

------------------------
PRESS 1 TO INSERT RECORD
PRESS 2 TO UPDATE RECORD
PRESS 3 TO DELETE RECORD
PRESS 4 TO DISPLAY RECORDS
PRESS 5 TO GO BACK
------------------------
ENTER YOUR CHOICE: 4
```

## 🛡️ Error Handling

All MySQL operations are wrapped in `try-except-finally` blocks to handle:
- Connection errors
- Query issues
- Proper resource cleanup (cursor and connection closing)

## 📌 Notes

- Be sure your MySQL tables match the expected schema.
- Modify field lengths/types in MySQL if needed to suit real-world data better.


---
