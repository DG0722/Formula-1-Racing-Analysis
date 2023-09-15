# F1 Analysis (Databricks, PySpark)
## Introduction
designing and orchestrating a data pipeline using Databricks and Azure to efficiently process, analyze, and visualize Formula 1 race results.
## Data Source
[Ergast Developer API](http://ergast.com/mrd/)
## ERD Diagram
![image](https://github.com/jdenggao/Databricks-Spark-Data-Pipeline/assets/112433825/f7dedb49-52d0-4716-acc7-68a87f38e910)
## Pipeline Architecture
![image](https://github.com/jdenggao/Databricks-Spark-Data-Pipeline/assets/112433825/ae6ba2f4-c99f-4198-9035-43b04a15bb11)
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

![image](https://github.com/jdenggao/Databricks-Spark-Data-Pipeline/assets/112433825/6a652558-8533-4b9d-9db2-57afdb359802)

![image](https://github.com/jdenggao/Databricks-Spark-Data-Pipeline/assets/112433825/0732a590-c703-4c95-9579-b29ee783252f)
