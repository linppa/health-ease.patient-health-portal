# HealthEase Patient Portal

* CS5200 Final Project - Fall 2023
* Group Name: QuinnNSaslowKQuachL
* Authors: Nicole Quinn, Kaitlyn Saslow, Linda Quach

---

# Introduction

HealthEase is a healthcare management application designed to offer patients a unified platform for accessing and managing their health-related information and services. The application is backed by a MySQL database named "health_ease," modeling a patient portal. It supports two user roles: patients and system administrators. Patients can view their doctors, appointment history, prescriptions, and billing information. System administrators can manage patient accounts, doctors, prescriptions, and more. Changes made in the CLI update the SQL database, and vice versa.

---

# Command Line Interface

Built in Python, the CLI (`health_ease_CLI.py`) guides users through the application. Upon execution, it prompts users to navigate the program using a main menu and command-line inputs.

<img src="images/main menu.png" width="600" />

---

# Technical Specifications

## Prerequisites

- **MySQL 8.0+**: [Download MySQL](https://dev.mysql.com/downloads/mysql/)
- **Python 3.7+**: [Download Python](https://www.python.org/downloads/)

## Files
- **SQL**
  - HealthEase_DB_Dump.sql: A self-contained database dump for MySQLWorkbench import.
- **Python**
  - health_ease_CLI.py: A command-line interface (CLI) for the application.
- README.md
- Final Report: QuinnNSaslowKQuachL_final_report.pdf

## Database Import Instructions

1. Use "HealthEaseDBDump-FINAL.sql" for database import.
2. In MySQLWorkbench, establish a connection and navigate to Server → Data Import.
3. Select "Import From Self-Contained File" and choose "HealthEaseDBDump-FINAL.sql".
4. Select "Dump Structure and Data" to complete the import.

<img src="images/sql db.png" width="600" />

## Python Environment Setup

Install the following Python packages:

```shell
pip install pymysql getpass datetime re matplotlib.pyplot seaborn
```

## Running the Application

1. Dump the database into MySQLWorkbench using "HealthEase_DB_Dump.sql".
2. Navigate to the directory containing "health_ease_CLI.py" in the terminal.
3. Run the following command:

```shell
python3 health_ease_CLI.py
```

<img src="images/sql log in.png" width="600" />

Upon launching the script, the instructor will be prompted to enter their SQL server credentials to establish a connection with the database. One a connection to the MySQL server is established successfully, the homepage of our patient portal HealthEase will be displayed and the user can get started.  

<img src="images/log in.png" width="600" />

---

# Alternative Log-in Access
## Patient Accounts
For testing operations that require a pre-existing prescription or bill, the following patient accounts can be used:

* John Doe: (username: john.doe@email.com, password: password123$)
* Jane Smith: (username: jane.smith@email.com, password: howdy123$)

## System Administrator Account
For testing the system administrator role of the application, the instructor can
log-in to the portal with the information below. A different menu will appear
which will expose the functionality of the program from the system
administrator's side, where you can view/delete patients, update patient
accounts, and view/add doctors.

* Portal Admin: (username: portaladmin@healthease.com, password: strongpass!)

---

# Application Interaction
Once all necessary Python libraries are installed, the CLI will guide the instructor through our database application. Depending on whether the instructor chooses to log-in to the portal as a patient or administrator, the menu that appears will be different. At each step of the program, the instructor will be guided and prompted with clear instructions for what to do/what information to enter. If information is entered incorrectly or an operation is not supported by the specific menu item selected, there are clear and descriptive error messages printed to the terminal so that the user can either try again, or select a different action from the menu.  

# Exiting the Program
At any time, the user can “exit” and navigate back to the main menu, where either “Q” or “q” can be typed in order to exit the program, which will terminal upon quitting.  
