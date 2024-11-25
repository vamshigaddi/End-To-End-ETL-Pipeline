
### Overview
This project demonstrates the design and implementation of a robust ETL (Extract, Transform, Load) pipeline for extracting weather data from an external API, processing it, and storing it in a database for analysis and reporting. The pipeline is orchestrated using Apache Airflow, leveraging its powerful DAG (Directed Acyclic Graph) capabilities for scheduling and automation.

### Tools and Technologies
- Apache Airflow: Workflow orchestration and task automation.
- Weather API: Any public or private weather API to fetch data.
- Python: For data extraction, transformation, and Airflow task scripts.
- Database: PostgreSQL for data storage.

### Project Contents

Your Astro project contains the following files and folders:

- dags: This folder contains the Python files for your Airflow DAGs. By default, this directory includes one example DAG:
    - `example_astronauts`: This DAG shows a simple ETL pipeline example that queries the list of astronauts currently in space from the Open Notify API and prints a statement for each astronaut. The DAG uses the TaskFlow API to define tasks in Python, and dynamic task mapping to dynamically print a statement for each astronaut. For more on how this DAG works, see our [Getting started tutorial](https://www.astronomer.io/docs/learn/get-started-with-airflow).
- Dockerfile: This file contains a versioned Astro Runtime Docker image that provides a differentiated Airflow experience. If you want to execute other commands or overrides at runtime, specify them here.
- include: This folder contains any additional files that you want to include as part of your project. It is empty by default.
- packages.txt: Install OS-level packages needed for your project by adding them to this file. It is empty by default.
- requirements.txt: Install Python packages needed for your project by adding them to this file. It is empty by default.
- plugins: Add custom or community plugins for your project to this file. It is empty by default.
- airflow_settings.yaml: Use this local-only file to specify Airflow Connections, Variables, and Pools instead of entering them in the Airflow UI as you develop DAGs in this project.

Deploy Your Project Locally

1. Start Airflow on your local machine by running 'astro dev start'.

This command will spin up 4 Docker containers on your machine, each for a different Airflow component:

- Postgres: Airflow's Metadata Database
- Webserver: The Airflow component responsible for rendering the Airflow UI
- Scheduler: The Airflow component responsible for monitoring and triggering tasks
- Triggerer: The Airflow component responsible for triggering deferred tasks

2. Verify that all 4 Docker containers were created by running 'docker ps'.

Note: Running 'astro dev start' will start your project with the Airflow Webserver exposed at port 8080 and Postgres exposed at port 5432. If you already have either of those ports allocated, you can either [stop your existing Docker containers or change the port](https://www.astronomer.io/docs/astro/cli/troubleshoot-locally#ports-are-not-available-for-my-local-airflow-webserver).

3. Access the Airflow UI for your local Airflow project. To do so, go to http://localhost:8080/ and log in with 'admin' for both your Username and Password.

You should also be able to access your Postgres Database at 'localhost:5432/postgres'.

### Airflow

- DAGs-Dashboard

![DAGs-Dashboard](Screenshot_dashboard.png)


- ETl-Dashboard

![etl-Dashboard](https://raw.githubusercontent.com/vamshigaddi/End-To-End-ETL-Pipeline-Using-Airflow/refs/heads/main/Screenshot%20_etl_dashboard.png)

- ETl-Graph
- 
![etl-graph](https://raw.githubusercontent.com/vamshigaddi/End-To-End-ETL-Pipeline-Using-Airflow/refs/heads/main/Screenshot%20-etl-graph.png)

- weather-data

![weather-data](https://github.com/vamshigaddi/End-To-End-ETL-Pipeline-Using-Airflow/blob/main/Screenshot%20-weather-data.png)

- Postgresql

![Postgressql-data](https://github.com/vamshigaddi/End-To-End-ETL-Pipeline-Using-Airflow/blob/main/Screenshot_Data_storage.png)
