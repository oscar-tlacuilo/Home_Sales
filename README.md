# Spark Data Analysis Project

## Overview

This project demonstrates data analysis using Apache Spark with a dataset containing home sales information. The dataset includes various attributes such as date sold, price, number of bedrooms, and more. The analysis involves creating Spark DataFrames, performing SQL queries, and optimizing performance through caching and partitioning.

## Setup

### Prerequisites

- Apache Spark
- Java Development Kit (JDK)
- Python with PySpark library
- Google Colab (for running notebooks)

## Dataset Description

The dataset used in this project contains information about home sales, including attributes such as the date of sale, the price of the home, number of bedrooms and bathrooms, square footage, and more. This data provides a comprehensive view of home sales, allowing for various types of analysis.

- `id`: Unique identifier for each home sale
- `date`: Date when the home was sold
- `date_built`: Year when the home was built
- `price`: Sale price of the home
- `bedrooms`: Number of bedrooms in the home
- `bathrooms`: Number of bathrooms in the home
- `sqft_living`: Square footage of the home
- `sqft_lot`: Square footage of the lot
- `floors`: Number of floors in the home
- `waterfront`: Whether the home is on the waterfront (1 if yes, 0 if no)
- `view`: View rating of the home
## Project Steps

1. **Create a Spark DataFrame**: 
   - Load the home sales dataset into a Spark DataFrame to facilitate processing and analysis.

2. **Create a Temporary Table**: 
   - Convert the Spark DataFrame into a temporary SQL table. This enables the use of SQL queries to interact with the data.

3. **Query Average Price for Four-Bedroom Houses**:
   - Write and execute a query to find the average price of four-bedroom houses sold each year. The result is rounded to two decimal places to provide a clear and concise insight.

4. **Query Average Price for Homes with Specific Features**:
   - Perform queries to calculate the average price of homes with three bedrooms and three bathrooms for each year. Additionally, refine the query to include homes with specific features such as two floors and a minimum square footage.

5. **Query Average Price per View Rating**:
   - Analyze the average price of homes based on their view rating, focusing on homes with an average price greater than or equal to $350,000. This query also includes performance measurement to assess runtime.

6. **Cache the Temporary Table**:
   - Implement caching for the temporary table to improve query performance. Caching stores intermediate results, which can significantly speed up repeated queries.

7. **Run Queries on Cached Data**:
   - Re-run the query from the previous step on the cached table and compare the performance to the uncached query to evaluate the benefits of caching.

8. **Partition Data and Write to Parquet**:
   - Partition the dataset by the year the home was built and write it to Parquet format. Parquet is an efficient columnar storage format that optimizes query performance.

9. **Read and Query Parquet Data**:
   - Read the partitioned Parquet data into a new DataFrame and create a temporary table for this data. Re-run the query from earlier steps to compare performance with the cached and uncached results.

10. **Uncache and Verify Table**:
    - Uncache the temporary table to free up resources and verify that the table is no longer cached. This step ensures that caching has been properly managed and resources are optimally used.

## Results

Throughout this project, various SQL queries were executed to extract valuable insights from the dataset. Key findings include:

- **Data Loading**: Successfully created a Spark DataFrame from the dataset.
- **Temporary Table Operations**: Effectively used SQL queries on temporary tables to analyze the data.
- **Caching Benefits**: Demonstrated the impact of caching on query performance, with noticeable improvements in execution times.
- **Parquet Optimization**: Showed how partitioning and using the Parquet format can enhance data processing and querying efficiency.
- **Performance Comparison**: Compared the runtimes of queries on cached and uncached data, as well as on Parquet files, providing insights into performance optimization.

## Conclusion

This project highlights the power of Apache Spark in handling large datasets and performing complex data analysis. By leveraging Spark’s capabilities for creating DataFrames, running SQL queries, and optimizing performance through caching and partitioning, the project successfully demonstrated how to efficiently process and analyze home sales data.
