# COVID-19 Data Analysis Capstone Project

The COVID-19 pandemic has had far-reaching consequences, causing significant loss of lives and disruptions to societies. This project delves into the analysis of sample data pertaining to COVID-19 cases recorded between January 2019 and December 2020.


# Project Overview
The dataset provided for this Project is in a CSV format and the database used in this project is PostgreSQL.

# The EL process extracts the data from the CSV file, loads it into a postgresql database and transforms it into a format that is more suitable for analysis.
the file describes how to extract a downloaded data link with the content named covid19_data, then create a table for the downloaded data link for some query task execution from the postgresql database.

## operational guidelines.

After extracting the file, before loading to the database, you need to set up the database and create a table name "covid_19_data"
create each of the columns accordingly to the extract downloaded covid_19_data file to avoid errors. 
to modify the column of the observationdate and change the data type from Text to DATE.
also drop the index column from the covid_19_data file which is not needed for this task.

# Table

CREATE TABLE covid_19_data(
index SERIAL,
Sno SERIAL PRIMARY KEY,
ObservationDate DATE, -------- **modification of the data type is been implemented here**
Province varchar(50),
Country varchar(50),
LastUpdate varchar(50),
Confirmed int,
Deaths int,
Recovered int
)

ALTER TABLE covid_19_data DROP COLUMN index;

**NB:** We were required to establish a database named 'covid_19_data' housing the dataset, which was done First before loading it to the postgres database.

## Requirements

** Python
** Pandas library
** SQLAlchemy library
** PostgreSQL database

**The ELT process is divided into the following steps:**

Extract: The data is extracted from the CSV file using Python script, requests api and pandas to read the csv file as a dataframe.

Load: The data is loaded into a postgresql database using SQLAlchemy as the connection tool.

Transform: The data is transformed in the postgresql database by cleaning it, removing outliers, and all queries analysis are executed.

# The Query Task

a. Retrieve the cumulative counts of confirmed, deceased, and recovered cases.

b. Extract the aggregate counts of confirmed, deceased, and recovered cases for the first quarter of each observation year.

c. Formulate a comprehensive summary encompassing the following for each
country:
Total confirmed cases
Total deaths
Total recoveries

d. Determine the percentage increase in the number of death cases from 2019 to 2020.

e. Compile data for the top 5 countries with the highest confirmed cases.

f. Calculate the net change (increase or decrease) in confirmed cases on a
monthly basis over the two-year period.


**outputs**
A directory within the repository, housing screenshots of the query outputs.


## Contribution and Feedback

Contributions and feedbacks are welcome to help us improve on the project.


