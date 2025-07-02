# Solaris Bank Loan ETL Demo

This is a simple ETL example using Apache Airflow to schedule a task that extracts loan data from the Snowflake data warehouse for Solaris Bank.

## Project Structure
- `Dags loan.py`: Airflow DAG file that runs the SQL query.
- `SQL loan.sql`: SQL script to extract outstanding loans.

## Tech Stack
- Apache Airflow (Workflow orchestration)
- Snowflake (Data warehouse)
- SQL (Data querying)

## How to Run
- Configure an Airflow connection to Snowflake, with connection ID `snowflake_default` (or change in the DAG as needed).
- Place this project in the Airflow DAGs folder.
- The DAG will run daily and extract all loans that are not closed.

---

