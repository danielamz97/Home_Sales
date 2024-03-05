# Spark SQL Analysis on Home Sales Data

This repository contains a Python script for analyzing home sales data using Apache Spark SQL. The script is designed to run on a Jupyter Notebook environment, such as Google Colab.

## Prerequisites
- Python 3.x
- Jupyter Notebook
- Apache Spark 3.x
- Java Development Kit (JDK) 11

## Setup Instructions
1. Clone this repository to your local machine.
2. Ensure you have Python 3.x installed along with Jupyter Notebook.
3. Install Apache Spark 3.x on your machine. You can download it from [the official Apache Spark website](http://spark.apache.org/downloads.html).
4. Install Java Development Kit (JDK) 11.
5. Open a Jupyter Notebook environment and navigate to the cloned repository directory.
6. Open the provided notebook file (.ipynb) in your Jupyter Notebook environment.
7. Run each cell in the notebook sequentially to execute the Spark SQL queries.

## Code Overview
- The script starts by setting up the Spark environment, installing necessary dependencies, and initializing a SparkSession.
- It then reads the home sales data from an AWS S3 bucket into a DataFrame and creates a temporary view of the DataFrame for running SQL queries.
- Several SQL queries are executed to analyze the home sales data, including calculating average prices based on different criteria.
- The script demonstrates caching of the temporary table for improved query performance and partitioning of data for further optimization.
- Each SQL query's runtime is measured to evaluate performance differences between cached and uncached data.

## Analysis of Results
1. **Average Price for Four Bedroom Houses per Year**: The analysis shows the average price of four-bedroom houses sold per year. The average prices fluctuate slightly across the years, indicating potential market trends or economic factors influencing home prices.
   
2. **Average Price of Homes by Year Built**: This query calculates the average price of homes based on the year they were built and filtered by three bedrooms and three bathrooms. The results show variations in average prices across different years, which could be influenced by factors like construction quality, location, or market demand.

3. **Average Price of Homes by Year Built, Bedrooms, Bathrooms, and Floors**: This query further narrows down the analysis by including additional criteria such as floors and square footage. It provides insights into the average prices of homes meeting specific criteria, allowing for more targeted market analysis.

4. **Average Price of Homes per View Rating**: The analysis examines the relationship between view ratings and home prices, focusing on properties with an average price equal to or greater than $350,000. The results reveal how view ratings correlate with higher-priced homes, which could be valuable information for property valuation and marketing strategies.

## Query Execution Times
- The notebook measures the runtime for each SQL query to assess performance differences between cached and uncached data.
- Cached queries generally exhibit faster execution times compared to uncached queries, indicating the benefits of caching for frequently accessed data.
- Partitioning the data can also improve query performance by reducing the amount of data processed, as demonstrated in the analysis using parquet-formatted data.

## Running in Google Colab
- This script is compatible with Google Colab. You can simply upload the notebook file to your Google Colab environment and run the cells.
- Ensure that you have sufficient resources allocated in your Google Colab environment for running Spark SQL queries, especially if working with large datasets.
- Follow the setup instructions provided in the notebook comments for installing Apache Spark and Java Development Kit (JDK) in your Google Colab environment.

## Notes
- Ensure that you have sufficient resources allocated to your Spark environment for running the queries, especially if working with large datasets.
- Modify the Spark configuration settings as needed based on your environment and requirements.

