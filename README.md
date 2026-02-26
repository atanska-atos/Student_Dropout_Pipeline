# Student_Dropout_Pipeline
Databricks pipeline for ingesting data into Data Lake, transforming data and creating materialized views ready to use for BI analysis.


Job Students_dropout has been created, containing 6 tasks:
- Bronze Layer:
1. Drop_table_if_exists - SQL query - dropping table if exists
2. Ingest_data_from_CSV - Notebook (pyspark) - ingesting data from raw CSV file and saving as a .parquet file
3. Create_table_bronze_layer - SQL query - creating new delta table from .parquet file
- Silver Layer
4. Data_Transformation_silver_layer - Notebook (pyspark) - transforming data as follow: data cleaning (mapping null values into average/median values), data standarization (changing various representation of the same mining data) and saving changes into delta table in the silver layer
- Gold Layer
5. Dropout_rate_per_Department - SQL query - creating materialized view with aggregated data
6. Average_GPA_per_Semester - SQL query - creating materialized view with aggregated data

<img width="1606" height="330" alt="image" src="https://github.com/user-attachments/assets/e8c76fe4-c504-48c6-9844-54375bfa0e7b" />
