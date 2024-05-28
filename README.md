# datafun-05-sql

Module 5 Project

Kersha Broussard May 27, 2024

Introduction: Professional project integrating Python and SQL

This project was built to the following specification: https://github.com/denisecase/datafun-05-spec


db_initialize_kershab.py
py -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install pandas pyarrow
py -m pip freeze > requirements.txt
# This .gitignore file lists content that does NOT need to be tracked in the project history

# Python virtual environment
.venv/

# Visual Studio Code settings and workspace
.vscode/

# Compiled Python files
__pycache__/
flask
requests
pandas
numpy
python -m pip install -r requirements.txt
def main():
    db_filepath = 'your_database.db'

    # Create database schema and populate with data
    execute_sql_from_file(db_filepath, 'insert_records.sql')
    execute_sql_from_file(db_filepath, 'update_records.sql')
    execute_sql_from_file(db_filepath, 'delete_records.sql')
    execute_sql_from_file(db_filepath, 'query_aggregation.sql')
    execute_sql_from_file(db_filepath, 'query_filter.sql')
    execute_sql_from_file(db_filepath, 'query_sorting.sql')
    execute_sql_from_file(db_filepath, 'query_group_by.sql')
    execute_sql_from_file(db_filepath, 'query_join.sql')

    logging.info("All SQL operations completed successfully")

import sqlite3
import pandas as pd
import pathlib
import logging

# Configure logging to write to a file, appending new logs to the existing file
logging.basicConfig(filename='log.txt', level=logging.DEBUG, filemode='a', format='%(asctime)s - %(levelname)s - %(message)s')

logging.info("Program started") # add this at the beginning of the main method
logging.info("Program ended")  # add this at the end of the main method
# Your code here....

def main():
    create_database()
    create_tables()
    insert_data_from_csv()

if __name__ == "__main__":
    main()
    
