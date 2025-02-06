# Data Engineering Project

This project focuses on building a data pipeline that transforms raw music data from a CSV file on Kaggle into a fully viusalized and queryable dashboard in metabase. The pipeline integrates multiple tools and techniques, including Airflow for automation, Soda for data quality checks, dbt for data tables, and BigQuery as the data warehouse. Each stage of the process is designed to ensure a scalable and insightful data flow.

### Pipleline Overview

- **Dataset**: A raw CSV file containing music related data (e.g. track details, album info, popularity) downloaded from Kaggle.
- **Airflow**: Used to orchestrate the pipeline, ensuring data is ingested, transformed, and loaded efficiently.
- **BigQuery**: Acts as the centralized data warehouse to store and query structured data.
- **Soda**: Implements data quality checks to validate the raw and tranformed data.
- **dbt**: Performs data transformations, creating cleaned and optimized tables for analysis.
- **Metabase**: Provides an interactive and user-friendly dashboard for visualizing key insights.

### Pipeline
<img width="1509" alt="Screenshot 2023-07-13 at 16 41 19" src="https://github.com/user-attachments/assets/e5639ba0-8b38-4f3f-a7a7-51dedaca9b3c" />

### VScode Screenshots
<img width="1502" alt="Screenshot 2025-02-06 at 12 55 26 PM" src="https://github.com/user-attachments/assets/eb1707e9-b26c-4beb-816f-f1b5a86cf4f0" />
<img width="792" alt="Screenshot 2025-02-06 at 12 56 53 PM" src="https://github.com/user-attachments/assets/30ef20ad-7938-425d-ba9a-8614cd4a30d1" />

**Note: Project involved sensitive data. Can't show all steps.**

### Code Map
```
├── dags/
│   ├── etl_pipeline.py           # Airflow DAG script
├── models/
│   ├── dim_datetime.sql          # dbt model for datetime dimension
│   ├── dim_track.sql             # dbt model for track dimension
│   ├── dim_artist.sql            # dbt model for artist dimension
│   ├── dim_playlist.sql          # dbt model for playlist dimension
│   ├── fct_music.sql             # dbt model for fact table
│   ├── dbt_project.yml           # dbt project configuration
│   ├── profiles.yml.example      # Example dbt profile for BigQuery
├── soda/
│   ├── soda_configuration.yml    # Soda configuration file
│   ├── soda_configuration.yml.example  # Example Soda config
├── metabase/
│   ├── dashboards.json           # Metabase JSON export (optional)
├── data/
│   ├── raw_music_data.csv        # Kaggle dataset (if not sensitive)
├── .gitignore                    # Files and folders to ignore in Git
├── README.md                     # Project documentation
├── requirements.txt              # Python dependencies
└── .env.example                  # Example environment variables
```

### Metabase Screenshot
![unnamed](https://github.com/user-attachments/assets/6c1ca166-2d49-4178-9bff-bfff435a51c3)
