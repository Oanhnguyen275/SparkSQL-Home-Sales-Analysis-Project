# SparkSQL_Home_Sales

Project Overview

This project involves using SparkSQL to analyze a dataset of home sales, focusing on key metrics such as average home prices by bedroom count, year built, view ratings, and specific conditions like square footage and number of floors. The project also includes working with Spark features such as creating temporary views, partitioning, caching, and uncaching tables for optimized performance.

Import necessary PySpark SQL functions to begin working with the data.
Load the dataset: Read the home_sales_revised.csv from the provided AWS S3 bucket location into a PySpark DataFrame.
Create a temporary table: Create a table named home_sales for use in SparkSQL queries.
Key Tasks

Average price for a four-bedroom house sold each year, rounded to two decimal places.
Average price of homes with three bedrooms and three bathrooms, grouped by the year they were built.
Average price of homes with three bedrooms, three bathrooms, two floors, and a minimum of 2,000 square feet, grouped by the year they were built.
Average price by "view" rating, for homes priced at or above $350,000. Include runtime for the query.
Advanced Steps
Cache the home_sales table and verify it is cached.
Re-run the "view" rating query on the cached data, and compare the runtime to the uncached query.
Partition the dataset by the "date_built" field, and save the data in Parquet format.
Create a temporary table for the Parquet data and run the "view" query again on it, comparing the runtime to previous queries.
Uncache the home_sales table and verify that it has been uncached.
