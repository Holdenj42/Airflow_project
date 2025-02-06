# Data Engineering Project

This project focuses on building a data pipeline that transforms raw music data from a CSV file on Kaggle into a fully viusalized and queryable dashboard in metabase. The pipeline integrates multiple tools and techniques, including Airflow for automation, Soda for data quality checks, dbt for data tables, and BigQuery as the data warehouse. Each stage of the process is designed to ensure a scalable and insightful data flow.

### Pipleline Overview

- **Dataset**: A raw CSV file containing music related data (e.g. track details, album info, popularity) downloaded from Kaggle.
- **Airflow**: Used to orchestrate the pipeline, ensuring data is ingested, transformed, and loaded efficiently.
- **BigQuery**: Acts as the centralized data warehouse to store and query structured data.
- **Soda**: Implements data quality checks to validate the raw and tranformed data.
- **dbt**: Performs data transformations, creating cleaned and optimized tables for analysis.
- **Metabase**: Provides an interactive and user-friendly dashboard for visualizing key insights.
