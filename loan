from airflow import DAG
from airflow.providers.snowflake.operators.snowflake import SnowflakeOperator
from datetime import datetime

with DAG(
    dag_id='solarisb_loan_etl',
    start_date=datetime(2025, 7, 1),
    schedule_interval='@daily',
    catchup=False,
    tags=['solarisb', 'loan', 'etl'],
) as dag:

    extract_loan = SnowflakeOperator(
        task_id='extract_loan_table',
        sql='sql/extract_loan.sql',
    )
