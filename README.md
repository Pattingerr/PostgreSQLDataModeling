# Data modeling with PostgreSQL

## Project description

Data modeling with Postgres and build an ETL pipeline using Python. Define fact and dimension tables for a star schema for a particular analytic focus, and write an ETL pipeline that transfers data from files in two local directories into these tables in Postgres using Python and SQL.

## Schema design and ETL pipeline

### Schema

#### Fact table

##### songplays
    - songplay_id
    - start_time
    - user_id
    - level
    - song_id
    - artist_id
    - sessions_id
    - location
    - user_agent
    
#### Dimension tables

##### time
    - start_time
    - hour
    - day
    - week
    - month
    - year
    - weekday
    
##### songs
    - song_id
    - title
    - artist_id
    - year
    - duration
    
##### users
    - user_id
    - first_name
    - last_name
    - gender
    - level
 
##### artists
    - artist_id
    - name
    - location
    - latitude
    - longitude

### Data Model

![db](https://github.com/Pattingerr/PostgreSQLDataModeling/blob/main/postgres_db.jpg)

## Files

**create_tables.py**

Python script to create postgres tables.

**etl.ipynb**

Jupyter Notebook for ETL testing.

**etl.py**

Python script to load data into postgres tables.

**sql_queries.py**

Python script with SQL-queries to create and query tables.

**test.ipynb**

Jupyter Notebook to test postgres data base.

## Run the project

The file create_tables.py creates the necessary tables to hold the data. After running this file and creating the tables, the file etl.py has the code to transfer the data from the data/ folder into the database.

