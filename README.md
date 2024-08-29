# F1 Analysis (Databricks, PySpark)
## Introduction
designing and orchestrating a data pipeline using Databricks and Azure to efficiently process, analyze, and visualize Formula 1 race results.
## Data Source
[Ergast Developer API](http://ergast.com/mrd/)
## ERD Diagram
![image](https://github.com/user-attachments/assets/e04f87d2-f749-4a36-a9ce-339ed408a10c)
## Pipeline Architecture
![image](https://github.com/user-attachments/assets/1feab16d-dabb-4be1-b51e-6812ab32d33f)
#### Data Raw Layer：
Data from the Ergest Developer API is initially imported into a raw Azure Data Lake Storage (ADLS) container.
#### Data Ingest Layer:
Employed Databricks notebooks to process raw data. Within this layer, we apply a schema to the data, store it in the efficient columnar Parquet format, and create partitions where applicable. Additionally, we incorporate supplementary information for audit purposes, including timestamps and the data source.
#### Data Presentation Layer:
Data is then transformed via Databricks notebooks to prepare it for the presentation layer. In this layer, we design and develop dashboards to meet our analytical requirements.
#### Orchestration and Monitoring Layer:
Azure Data Factory is employed to schedule and monitor the entire pipeline, ensuring its reliability and efficiency.
#### Delta Lakehouse Architecture:
As part of the project's evolution, we transition the pipeline into the Delta Lakehouse architecture. This adaptation addresses specific needs related to GDPR compliance, time-travel capabilities, and other essential requirements.
## Results
![image](https://github.com/user-attachments/assets/8e815b2b-a0b0-4860-b5e7-482c9d1c4bef)

![image](https://github.com/user-attachments/assets/c7987773-ee25-4d0d-a0df-5c381d38ba86)

