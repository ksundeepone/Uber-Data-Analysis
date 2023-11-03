# Uber Data Pipeline Project
This repository contains the code and documentation for my Uber Data Pipeline project. In this project, I've extracted the Yellow Cab dataset from NYC.Gov for the year 2023 and transformed the data using Python in a Jupyter notebook. The transformed data is stored in a Google Cloud Storage bucket.

#### Tools used: 

### - **Google Cloud** 
> (BigQuery, Cloud Storage, Compute Engine)

### - **Mage** (The modern replacement for Airflow)
> (Mage is an open-source data pipeline tool for integration and transforming data.)

### - **Looker Studio**
> Data Visualization


## Features :-

1. **Data Validation and Cleansing**: Implement a data validation step to ensure data quality and consistency, and add data cleansing processes to handle missing or incorrect data.

2. **Data Partitioning**: Optimize the data storage in BigQuery by partitioning the data based on time, region, or other relevant factors to improve query performance.

3. **User Access Control**: Implement fine-grained access control for data in BigQuery, ensuring that only authorized users can access specific datasets and tables.

4. **ETL Automation**: Schedule ETL jobs to run at specific intervals or in response to specific events, reducing manual intervention.

5. **Version Control for Pipeline Code**: Use version control for your data pipeline code and configurations to track changes, collaborate with team members, and ensure reproducibility.

6. **API Authentication**: Enhance security by implementing proper authentication and authorization mechanisms for accessing external APIs and services.
