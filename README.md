# Home_Sales
mod 22



This script includes an iPython notebook that uses Spark to analyze and visualize home sales data.

The script begins by importing PySpark SQL functions and reading home sales data from a CSV file using Spark. It proceeds to create a temporary table view named 'home_sales'. Subsequently, it leverages Spark SQL to extract the following insights from the table:

The average sale price of four-bedroom homes for each year.
The average sale price each year for homes built in that year, which have three bedrooms and three bathrooms.
The average sale price each year for homes that were built in that year, featuring three bedrooms, three bathrooms, two floors, and a minimum of 2,000 square feet.
The average sale price for homes by 'view' rating, specifically for those with an average price of at least $350,000, along with the execution time for this query.
After these analyses, the 'home_sales' table is cached. The script then re-executes the last query using the cached data and displays the runtime to highlight any performance improvements. Following this, it partitions the home sales data by the 'date_built' field into a formatted parquet file, creates a temporary table for this data, and runs the last query again to compare the runtime against the cached data. Finally, the script uncaches the 'home_sales' temporary table.
