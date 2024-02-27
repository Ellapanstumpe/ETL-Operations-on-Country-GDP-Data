# ETL-Operations-on-Country-GDP-Data
This Python script performs ETL (Extract, Transform, Load) operations on country-wise GDP data from a Wikipedia page. The data is extracted, transformed, and saved to both a CSV file and a SQLite database.

Table of Contents

Introduction
Prerequisites
Usage
Functions
Logging
Example Query

1. Introduction <a name="introduction"></a>
This script fetches GDP data for various countries from a Wikipedia page, performs necessary transformations, and saves the results to a CSV file and a SQLite database. The script is modular, making it easy to understand and extend for different use cases.


3. Prerequisites <a name="prerequisites"></a>
Before running the script, ensure you have the required Python libraries installed:

wget https://en.wikipedia.org/wiki/List_of_countries_by_GDP_(nominal)
python3.11 -m pip install pandas
python3.11 -m pip install numpy
python3.11 -m pip install bs4

3. Usage <a name="usage"></a>
To execute the script, simply run: 


  python your_script_name.py

4. Functions <a name="functions"></a>
4.1 extract(url, table_attribs)
Extracts country-wise GDP data from a Wikipedia page.

4.2 transform(df)
Transforms GDP data from currency format to a float value and converts GDP from USD (Millions) to USD (Billions).

4.3 load_to_csv(df, csv_path)
Saves the final dataframe as a CSV file.

4.4 load_to_db(df, sql_connection, table_name)
Saves the final dataframe to a SQLite database table.

4.5 run_query(query_statement, sql_connection)
Runs a SQL query on the database table and prints the output.

4.6 log_progress(message)
Logs messages at different stages of the code execution to a log file.

5. Logging <a name="logging"></a>
Execution progress and key messages are logged to a file named "etl_project_log.txt" in the script's directory.

6. Example Query <a name="example-query"></a>
An example SQL query is included in the script to retrieve countries with GDP greater than or equal to $100 billion.

7. License <a name="license"></a>
This script is licensed under the MIT License - see the LICENSE file for details.

Feel free to customize the script for your specific use case or data sources.

For any issues or questions, please refer to the documentation of the libraries used or seek assistance from relevant forums.
