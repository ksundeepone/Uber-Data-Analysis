# Uber Data Pipeline Project
This repository contains the code and documentation for my Uber Data Pipeline project. In this project, I've extracted the Yellow Cab dataset from NYC.Gov for the year 2023 and transformed the data using Python in a Jupyter notebook. The transformed data is stored in a Google Cloud Storage bucket.
#### Tools used: 
### - **Google Cloud** 
> (BigQuery, Cloud Storage, Compute Engine)
### - **Mage** (The modern replacement for Airflow)
> Mage is a modern replacement for **Airflow**, It is an open-source data pipeline tool for integration and transforming data.
> https://www.mage.ai
> https://github.com/mage-ai/mage-ai
### - **Looker Studio**
> Data Visualization


## Features :-

1. **Data Validation and Cleansing**: Implement a data validation step to ensure data quality and consistency, and add data cleansing processes to handle missing or incorrect data.

2. **Data Partitioning**: Optimize the data storage in BigQuery by partitioning the data based on time, region, or other relevant factors to improve query performance.

3. **User Access Control**: Implement fine-grained access control for data in BigQuery, ensuring that only authorized users can access specific datasets and tables.

4. **ETL Automation**: Schedule ETL jobs to run at specific intervals or in response to specific events, reducing manual intervention.

5. **Version Control for Pipeline Code**: Use version control for your data pipeline code and configurations to track changes, collaborate with team members, and ensure reproducibility.

6. **API Authentication**: Enhance security by implementing proper authentication and authorization mechanisms for accessing external APIs and services.


Here's a step-by-step process for your Uber data pipeline project:

**Step 1: Data Extraction and Transformation**
- Download the yellow cab dataset for the year 2023 from NYC.Gov.
- Load the dataset into the Jupyter notebook.
- Use Python to perform necessary data transformations, such as cleaning, filtering, and structuring the data as needed for your project.


**Step 2: Data Storage Setup**
- Log in to your Google Cloud account and navigate to Google Cloud Storage.
- Create a new bucket in Google Cloud Storage to store your transformed data.
- Change the Dataset Firewall to Fine-grained to get public access.

**Step 3: Virtual Machine and Mage Setup**
- Set up a Virtual Machine (VM) in Google Cloud to use as the host for your data pipeline.
- Install the Mage data pipeline tool on the VM. You may need to follow the installation instructions provided by Mage.
- Configure Mage with the necessary credentials and permissions to access your Google Cloud Storage bucket and BigQuery.

**Step 4: Data Pipeline Creation**
- Launch Mage on your VM and create a data pipeline for your project.
- Define the pipeline stages, including loading, transformation, and exporting.
- For the loading stage, use Mage's Loader function to connect to your Google Cloud Storage bucket and ingest the transformed data.

  <img width="1440" alt="Screenshot 2023-11-03 at 1 16 40 AM" src="https://github.com/ksundeepone/Uber-Data_Pipeline-Project/assets/102394204/0076ef6b-e4d7-43b0-80dc-a0a8f5713402">


<img width="1440" alt="Screenshot 2023-11-03 at 1 16 16 AM" src="https://github.com/ksundeepone/Uber-Data_Pipeline-Project/assets/102394204/8de2496e-9761-4c88-927a-f92b7960be25">



**Step 5: Google Cloud Integration**
- In the Google Cloud Console, navigate to the API & Services section.
- Create the necessary credentials and permissions to allow Mage to access your BigQuery project.
- Configure the Mage pipeline to connect to BigQuery using the credentials created in the previous step.

**Step 6: Data Export and Analysis**
- Execute the Mage data pipeline, which will load the data from your Google Cloud Storage bucket, transform it, and export it to BigQuery.
- Access BigQuery and run SQL queries to analyze and manipulate the data as required for your project.
- Use the results of your analysis to create reports and dashboards in Looker Studio or any other preferred data visualization tool.


## Python Installation in VM

```sh
sudo apt-get update -y
sudo apt-get install python3-distutils
sudo apt-get install python3-apt
sudo apt-get install wget
wget https://bootstrap.pypa.io/get-pip.py
sudo python3 get-pip.py
```



## Mage Installation in VM

Install Mage in VM instances using the below code from SSH.

```sh
pip install mage-ai (or)
conda install -c conda-forge mage-ai
mage start demo_project
```
- Create a Firewall to access Mage through the external port

```
