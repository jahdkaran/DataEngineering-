# Data Gathering Methods and Tools

Learn about methods and tools for gathering and importing data from various sources.

## Data Gathering Methods

- **SQL**: Query relational databases.
- **Non-relational Databases**: Use SQL-like tools (e.g., CQL, GraphQL).
- **APIs**: Extract data from endpoints.
- **Web Scraping**: Extract data from web pages.
- **RSS Feeds**: Capture updated data.
- **Data Streams**: Aggregate data from IoT devices and social media.
- **Data Exchange Platforms**: Facilitate secure data exchange (e.g., AWS Data Exchange).

## Data Importing

- **Relational Databases**: Store structured data.
- **NoSQL Databases**: Store structured, semi-structured, and unstructured data.
- **Data Lakes**: Accommodate all data types.

## Tools and Methods

- **ETL Tools**: Automate data importing (e.g., Talend, Informatica).
- **Programming Languages**: Use Python and R for data importing.

Data from various sources is loaded into repositories for analysis, with tools chosen based on data type and volume.

## Data Wrangling

Raw data must be transformed and cleansed to be analytics-ready. Data wrangling, or data munging, involves:

- **Structuring**: Changing the form and schema of data, using joins and unions to combine data from different sources.
- **Normalization**: Reducing redundancy and inconsistency in data.
- **Denormalization**: Combining data from multiple tables for faster querying.

### Key Transformations

- **Cleaning**: Fixing irregularities in data.
  - **Detect Issues**: Use scripts, data profiling, and visualization tools to find anomalies.
  - **Common Issues**:
    - **Missing Values**: Filter, source, or impute missing data.
    - **Duplicate Data**: Remove repeated data points.
    - **Irrelevant Data**: Exclude data not relevant to the use case.
    - **Data Type Conversion**: Ensure values match the field's data type.
    - **Standardization**: Uniform formats for strings, dates, and units.
    - **Syntax Errors**: Fix white spaces, typos, and format inconsistencies.
    - **Outliers**: Identify and address values vastly different from others.

Data profiling and visualization help identify issues for cleaning, ensuring data is ready for meaningful analysis.


## Tools for Data Wrangling

Popular data wrangling tools include:

- **Spreadsheets**: Microsoft Excel and Google Sheets with add-ins like Power Query and Google Sheets Query.
- **OpenRefine**: Open-source tool for importing, exporting, and transforming data.
- **Google DataPrep**: Cloud service for exploring, cleaning, and preparing data.
- **Watson Studio Refinery**: IBM tool for discovering, cleansing, and transforming data.
- **Trifacta Wrangler**: Cloud-based service for cleaning and transforming data.
- **Python**: Libraries like Jupyter Notebook, Numpy, and Pandas for data manipulation.
- **R**: Libraries like Dplyr, Data.table, and Jsonlite for data wrangling.

Each tool offers unique features and capabilities, and the choice depends on specific use cases, infrastructure, and team requirements.

- **Trifacta Wrangler**: Cloud-based service for cleaning and transforming data.
- **Python**: Libraries like Jupyter Notebook, Numpy, and Pandas for data manipulation.
- **R**: Libraries like Dplyr, Data.table, and Jsonlite for data wrangling.

Each tool offers unique features and capabilities, and the choice depends on specific use cases, infrastructure, and team requirements.

## Basic Querying Techniques for Data Analysis

Learn about basic querying techniques for analyzing data in a database, applicable to SQL and other query languages.

### Key Techniques

- **Counting and Aggregating**:
  - `COUNT()`: Count the number of rows.
    ```sql
    SELECT COUNT(*) FROM customers;
    ```
  - `DISTINCT()`: Count unique values.
    ```sql
    SELECT DISTINCT(dealer) FROM sales;
    ```
  - `SUM()`: Calculate the sum of a numeric column.
    ```sql
    SELECT SUM(price) FROM sales;
    ```
  - `AVG()`: Calculate the average value.
    ```sql
    SELECT AVG(price) FROM sales;
    ```
  - `STDDEV()`: Measure the spread of numbers.
    ```sql
    SELECT STDDEV(price) FROM sales;
    ```

- **Identifying Extreme Values**:
  - `MAX()`: Find the maximum value.
    ```sql
    SELECT MAX(price) FROM sales;
    ```
  - `MIN()`: Find the minimum value.
    ```sql
    SELECT MIN(price) FROM sales;
    ```

- **Slicing Data**:
  - Use conditions to retrieve specific subsets of data.
    ```sql
    SELECT * FROM customers WHERE city = 'New York';
    ```

- **Sorting Data**:
  - `ORDER BY()`: Sort data in ascending or descending order.
    ```sql
    SELECT * FROM sales ORDER BY purchase_date DESC;
    ```

- **Filtering Patterns**:
  - `LIKE()`: Perform partial matches using patterns and wildcards.
    ```sql
    SELECT * FROM customers WHERE zipcode LIKE '123%';
    ```

- **Grouping Data**:
  - `GROUP BY()`: Group data and perform aggregate functions like `SUM()`.
    ```sql
    SELECT zipcode, SUM(price) FROM sales GROUP BY zipcode;
    ```

These techniques help in understanding and analyzing data effectively.

### Data Engineer Responsibilities

- **Monitoring and Optimizing Systems**: Ensure performance and availability.
- **Data Pipelines**: Manage data flow from source to destination.

### Performance Threats

- Scalability issues.
- Application failures.
- Scheduling issues.
- Tool incompatibilities.

### Performance Metrics

- **Latency**: Request fulfillment time.
- **Failures**: Service failure rate.
- **Resource Utilization**: Usage patterns.
- **Traffic**: User requests.

### Troubleshooting Steps

1. Collect incident information.
2. Verify software versions.
3. Check logs and metrics.
4. Reproduce issue in test environment.
5. Validate root cause.
6. Plan production deployment.

### Database Performance Metrics

- System outages.
- Capacity utilization.
- Application slowdown.
- Query performance.
- Conflicting activities.

### Optimization Best Practices

- **Capacity Planning**: Optimal resource determination.
- **Indexing**: Fast data location.
- **Partitioning**: Divide large tables.
- **Normalization**: Reduce redundancy.

### Monitoring Systems

- **Database Monitoring**: Track performance indicators.
- **Application Performance Management**: Measure response time and errors.
- **Query Performance Monitoring**: Gather statistics.
- **Job-Level Monitoring**: Monitor job steps.

### Maintenance Routines

- **Time-Based**: Scheduled activities.
- **Condition-Based**: Issue-specific activities.

### Summary

- Performance tuning and troubleshooting.
- Monitoring and alerting systems.
- Maintenance schedules.