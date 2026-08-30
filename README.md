# Tokyo Olympics Data Engineering Project

An end-to-end data engineering project built using Microsoft Azure.

This project takes Tokyo Olympics data from GitHub, ingests the data into Azure Data Lake Storage using Azure Data Factory, transforms the data using Azure Databricks and PySpark, and then uses Azure Synapse Analytics for SQL-based analysis.

## Technologies Used

* Azure Data Factory
* Azure Data Lake Storage Gen2
* Azure Databricks
* Apache Spark / PySpark
* Azure Synapse Analytics

## Project Architecture

```text
GitHub
   ↓
Azure Data Factory
   ↓
Azure Data Lake Storage Gen2
   ↓
Azure Databricks + PySpark
   ↓
Transformed Parquet Data
   ↓
Azure Synapse Analytics
   ↓
SQL Analysis
```

## Datasets

The project uses five Tokyo Olympics datasets:

* Athletes
* Coaches
* EntriesGender
* Medals
* Teams

## Project Workflow

1. Source CSV files are stored in GitHub.
2. Azure Data Factory retrieves the files using HTTP.
3. The raw CSV files are stored in the `raw-data` folder in ADLS Gen2.
4. Azure Databricks reads the raw files using PySpark.
5. Data types and other basic transformations are applied.
6. The transformed datasets are written as Parquet files.
7. The transformed data is stored in the `transformed-data` folder.
8. Azure Synapse Analytics is used to perform SQL analysis.

## What I Learned

Through this project, I gained hands-on experience with:

* Building data ingestion pipelines using Azure Data Factory
* Working with Azure Data Lake Storage Gen2
* Creating and using Databricks Spark clusters
* Reading CSV data using PySpark
* Performing basic data transformations
* Working with Spark DataFrames and schemas
* Writing transformed data as Parquet
* Using Azure Synapse Analytics for SQL analysis
* Understanding how different Azure services work together in a data engineering pipeline

## Conclusion

This project helped me understand how an end-to-end cloud data engineering pipeline can be built using Azure services.

The overall pipeline is:

**GitHub → Azure Data Factory → ADLS Gen2 → Databricks/PySpark → Transformed Parquet → Synapse Analytics**
