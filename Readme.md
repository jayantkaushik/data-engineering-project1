# Data Engineering Project
### Project Name: Data Engineering Project on the Databricks platform. 
#### Dataset: Car Sales Around the World

Description: This project is about performing data engineering(building pipelines, performing ETL ops etc.) using the Databricks platform. The result is an end-to-end automated data pipeline to structure the incoming data from the sample raw data set of car sales around the world.

#### Tech Stack Used:
  1. Apache Nifi
  2. Databricks
  3. Apache Spark
  4. PostgreSQL
  5. Python
  6. AWS S3

Steps performed:
  (steps not included in this repository due to technical roadblocks)
  #### Apache NiFi - A snip of the flow created:
  ![alt text](https://github.com/jayantkaushik/data-engineering-project1/blob/main/NiFi%20DEA%20Capture.JPG "NiFi Flow")
  
  1. Building a NiFi flow to automaticallyt fetch the files from SFTP whenever they are available/updated
  2. Putting the files in an AWS S3 bucket
  3. Also, putting the metadate of the files in a PostgreSQL table
  
  steps included in this repository - See notebook for code: [Jayant_kaushik.ipynb](https://github.com/jayantkaushik/data-engineering-project1/blob/main/Jayant_kaushik.ipynb)
  #### ETL Steps: (Extract, Transform and Load) using Apache Spark(PySpark):
  1. Creating a fact table(only for the initial run, will be ignored when subsequent files are recieved)
  2. Importing data from the CSV files fetched in S3 bucket
  3. Creating Dataframes for all the CSV files using Apache Spark
  4. Joining all the Dataframes to create a unified dataframe
  5. Performing other transformations like cleansing columns, concatenating where required, changing formats
  6. Making a final dataframe and converting it into a SQL temp view using Spark
  7. Merging this tempview with the Fact table
  8. Querying the final Fact table to run analysis on the data set and draw insights(e.g. Top selling cars, Top Revenue areas, Top Customers etc.)
  9. Creating a dashboard to present these insights in a visualised manner

----- end of data engg. ops. ----
