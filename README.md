# Context

The purpose of this project is to model in a SQL database all the logs of Sparkify app, in order to help the Analystics team to understand how the users are using our app and what songs are they listening to.

# Database Schema

We are using a Postgres database following the Star Schema desing. Some of the benefits of using this design are : 

- The data is denormalized which help in performance while querying the data.
- The queries to retreive needed information are relatively simple
- Simplified business reporting logic

# ETL pipeline

One the database designed and the tables created, a python script run the ETL pipeline to extract, transform and load all the log data found in json files under the `data` folder

# How to run scripts

In order to build the database you should: 

- Create the necessary tables by running the python script: `python3 create_table.py`
- Running the ETL pipelin with `python3 etl.py`
