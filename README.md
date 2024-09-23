# Tokyo Olympics Data Engineering Project 🏅

![Olympics](https://github.com/vedanthv/data-engineering-projects/assets/44313631/d8ddf328-5010-4e41-8dc4-5e695def87e3)

## Project Overview

This project showcases a comprehensive data pipeline built to ingest, transform, and analyze data from the 2021 (2020) Tokyo Olympics. The dataset includes information on **over 11,000 athletes**, **47 disciplines**, and **743 teams**. The primary goal of this project was to design a scalable, efficient, and cloud-native solution using **Azure Data Engineering** tools to enable actionable insights through **Power BI** dashboards.

## Dataset Details

The dataset contains:
- Athletes' names, disciplines, and countries.
- Gender and team participation.
- Coaches' details for the respective disciplines.
- Entries categorized by gender.

This rich dataset provided a foundation for a wide range of analyses, from gender representation to country-level performance metrics.

## Tech Stack

The following Azure tools and technologies were used to implement the end-to-end pipeline:
- **Azure Data Factory (ADF)**: For orchestrating the data movement.
- **Azure Data Lake Gen 2**: For storing raw and transformed data at scale.
- **Azure Blob Storage**: As a staging area for data ingestion.
- **Azure Databricks**: For advanced data transformation and processing using Spark.
- **Azure Synapse Analytics**: For integrating big data and performing further SQL analytics.
- **Power BI**: To visualize and generate insights from the data.

## Data Pipeline Architecture

![Pipeline Architecture](https://github.com/vedanthv/data-engineering-projects/assets/44313631/d0eeb64e-b6c9-40c8-bfde-413981d5fe0e)

The architecture includes:
1. **Data Ingestion**: Raw data from GitHub is ingested into Azure Blob Storage using Azure Data Factory.
2. **Data Transformation**: Using Databricks notebooks, the raw data is transformed into a clean and structured format, suitable for further analysis.
3. **Data Storage**: Transformed data is stored in Azure Data Lake Gen2 for long-term access and scalability.
4. **Data Analytics**: Using Synapse Analytics and Power BI, the data is queried, analyzed, and visualized.

## Setup Instructions

1. **Azure Setup**: Utilize the GitHub Student Pack to create an Azure account and enable necessary services.
2. **Repository Preparation**: Fork and clone the [GitHub repository](https://github.com/Rahul-Patel321/Tokyo-Olympic-azure-data-engineeering-project/tree/main/datasets) with the Olympics raw data.
3. **Databricks Integration**: No additional setup is required for Azure Databricks as it is single sign-on (SSO) authenticated with Azure.
4. **Storage Configuration**: Create a storage account on Azure and configure the Blob Storage container. Ensure it has the necessary read/write permissions via the IAM console.

## Data Ingestion

The raw data, hosted in a GitHub repository, is ingested into **Azure Blob Storage** using **Azure Data Factory**. The ingestion process ensures that the data is efficiently moved from source to cloud, maintaining data quality and integrity.

![Data Ingestion](https://github.com/vedanthv/data-engineering-projects/assets/44313631/e432b1af-4513-402e-865e-430404046de1)

## Data Transformation

The transformation phase was carried out using **Azure Databricks**, leveraging **PySpark** for large-scale data processing. Key transformation steps include:
- **Data Cleansing**: Removing duplicates and invalid entries.
- **Data Normalization**: Restructuring the dataset to be analytics-friendly.
- **Deriving Insights**: Creating new fields such as total medals, gender ratios, and country-wise performance.

The transformed data is then stored in **Azure Data Lake Gen2** for persistent storage.

![Data Transformation](https://github.com/vedanthv/data-engineering-projects/assets/44313631/05cbdf20-926c-4c67-a046-ec6f8ea2ed60)

### Transformed Data Stored in Azure Data Lake Gen2

![Transformed Data](https://github.com/vedanthv/data-engineering-projects/assets/44313631/6003970a-dd0b-45e7-80d9-696b64b4774b)

## Data Analytics and Visualization

With the transformed data stored in the lake, **Azure Synapse Analytics** was used to perform advanced queries and generate insights. For visualization, **Power BI** dashboards were created, enabling stakeholders to explore:
- **Athlete Performance**: Medal tally, top-performing countries, and athlete comparison.
- **Gender Representation**: Analyzing participation rates by gender across various sports.
- **Country-Wise Performance**: Insights into which countries dominated in specific disciplines.

### Dashboards and Reports

The final dashboards provide an interactive platform for decision-makers to drill down into specific metrics. The Power BI reports highlight key trends and patterns, offering valuable insights into Olympic performance.

![S - 1 (1)](https://github.com/user-attachments/assets/ba5dd66a-2096-44ab-b987-3ac8b577ded7)
![S - 1 (2)](https://github.com/user-attachments/assets/47199587-7c9b-4c26-ba86-d235900bc737)


Live Dashboard : https://app.powerbi.com/view?r=eyJrIjoiMTI4OGY4NmMtYWZmMC00OGYyLTkyYzMtNjA2NDhiZmY1NjE1IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9



## Databricks Transformation Code

The full data transformation code implemented in **Azure Databricks** can be accessed [here](https://github.com/Rahul-Patel321/Tokyo-Olympic-azure-data-engineeering-project/blob/main/Tokyo%20Olympic%20Transformation.ipynb).
