# Home Sales Analysis with PySpark

## Overview

This project demonstrates the use of SparkSQL and PySpark to analyze a dataset of home sales. The goal is to determine key metrics related to home prices based on various property features and to optimize query performance using Spark’s caching and partitioning features.

## Files

- `Home_Sales.ipynb`: Main notebook containing the full analysis.
- `home_sales_revised.csv`: The dataset used for analysis, sourced from an AWS S3 bucket.

## Instructions

1. Rename the `Home_Sales_starter_code.ipynb` file to `Home_Sales.ipynb`.
2. Import the necessary PySpark SQL functions.
3. Read the `home_sales_revised.csv` into a PySpark DataFrame.
4. Create a temporary table named `home_sales`.

## Analysis Tasks

Using SparkSQL, the following queries and tasks were completed:

1. Calculate the **average price** for four-bedroom homes sold in each year. Results are rounded to two decimal places.
2. Determine the **average price** of homes with **three bedrooms and three bathrooms** for each year the home was built.
3. Determine the **average price** of homes with:
   - Three bedrooms  
   - Three bathrooms  
   - Two floors  
   - At least 2,000 square feet  
   For each year the home was built.
4. Compute the **average price per "view" rating** for homes with an average price of **$350,000 or greater** and measure the **runtime**.
5. **Cache** the `home_sales` temporary table.
6. **Verify** that the table is cached.
7. **Re-run** the query from step 4 using the cached table and compare the **runtime**.
8. **Partition** the home sales data by the `date_built` field and save it as **Parquet**.
9. Create a **temporary table** from the Parquet data.
10. Re-run the query from step 4 using the Parquet table and compare the runtime.
11. **Uncache** the `home_sales` temporary table.
12. **Verify** that the table is uncached.

## Getting Started

To run this notebook:

1. Ensure you have Java (version 8 or 11), PySpark, and Jupyter Notebook installed.
2. Set the `JAVA_HOME` environment variable if needed.
3. Launch Jupyter Notebook and open `Home_Sales.ipynb`.
   
---

# Acknowledgements:

Special thanks to Dr. Carl Arrington for guidance during the Big Data Module. Some snippets and logic were developed following in-class tutorial support and discussions on the following topics: Querying Big Data with PySpark, Optimizing Spark: Storage, Partitioning, and Caching, and Databricks.
