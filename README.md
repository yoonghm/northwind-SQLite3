# Northwind-SQLite3

This is a version of the Microsoft Access 2000 Northwind sample database, re-engineered for SQLite3.

The Northwind sample database was provided with Microsoft Access as a tutorial schema for managing small business customers, orders, inventory, purchasing, suppliers, shipping, and employees. Northwind is an excellent tutorial schema for a small-business ERP, with customers, orders, inventory, purchasing, suppliers, shipping, employees, and single-entry accounting.

All the TABLES and VIEWS from the MSSQL-2000 version have been converted to Sqlite3 and included here. Included is a single version prepopulated with data. Should you decide to, you can use the included python script to pump the database full of more data.

[Download here](https://raw.githubusercontent.com/jpwhite3/northwind-SQLite3/master/dist/northwind.db)

# Structure

![alt tag](https://raw.githubusercontent.com/jpwhite3/northwind-SQLite3/master/images/Northwind_ERD.png)

# Build Instructions

## Prerequisites

- Python 3.6 or higher (`python3 --version`)
- SQLite3 installed `sqlite3 -help`

## Build

For Unix-like operating systems:

```console
sqlite3 northwind.db < create.sql > /dev/null
sqlite3 northwind.db < update.sql > /dev/null
sqlite3 northwind.db < report.sql
python3 populate.py
sqlite3 northwind.db < report.sql
```

For Windows OS:
```console
sqlite3 northwind.db < create.sql > NUL
sqlite3 northwind.db < update.sql > NUL
sqlite3 northwind.db < report.sql
python populate.py
sqlite3 northwind.db < report.sql
```
