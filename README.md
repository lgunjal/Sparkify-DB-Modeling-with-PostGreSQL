# Introduction
The project seeks to analyze song data collected by sparkify through its streaming app. One of the major focus is on the songs that are popular among the users. The data resides in JSON files and cannot be directly queried for analytical purposes. The purpose of this project is to make this data available to the end user in an easy to use and readily available format. Hence it has been decided that a relational database is best for these purposes.

# Project Scope
The aim of the project is to extract all available song data from JSON files and store it in a relational database for further analysis. The DBMS chosen for this project is PostgreSQL. The process, reads song data and log data from JSON files, performs ETL and stores it in a relational database with STAR Schema on PostgreSQL database namely SparkifyDB.

# Schema

## Fact Tables

### songplays :
A log table that records songplay data that describes location, time and other attributes of the songs played by a user.

## Dimension Tables

### users :
A table of user data containing id, name, gender and level of the user account.

### songs 
A table containing song attributes like title, artist, year and duration.

### artists 
A table containing artist information like name and location.

### time
Timestamp table of time column in the songplay table that is more granular in its time components.


# Working principle 
The program consists of 3 main working components , they are "create_tables.py" , "sql_queries.py" and 'etl.py'
The sql_queries.py file contains all table definitions. It also contains drop commands as well as the insert commands. All SQL queries in this program are written in this file.
The create_tables.py file has functions within itself that actually creates the database and the tables utilizing the queries from sql_queries.py.
The etl.py file contains functions that utilize the insert queries from sql_queries.py and insert records into the tables.


# Files list
## sql_queries.py 
Contains all SQL queries used in this program. Contains table definitions and drop statements.

## create_tables.py 
Drops and creates the defined tables.

## etl.ipynb 
Used for initial testing and debugging of code. Utilises single file from each of the data and log folders.

## test.ipynb 
Used to check if the create and insert operations are succesful.

## etl.ipynb 
Contains actual production code that populates all tables when it is run.

