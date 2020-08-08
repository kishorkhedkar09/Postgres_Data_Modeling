# Project-1: Data Modeling with Postgres
---
## Purpose of the project
This project deals with Data modeling with Postgres and populating the designed tables by building the ETL pipeline using python. The source data is from music streaming App called Sparkify. It is in two different parts - one is songs metadata and second is user activity logs. The complete dataset is in JSON format. The purpose of project is to design Star schema consisting fact and dimension tables which is used for songs and user activity analysis.

---

## Database schema design and ETL pipeline
The source data is modelled into star schema, consisting one fact table - songplays and four dimention tables - users, songs, artist, time. SQL commands (SELECT, CREATE, INSERT, DROP) are defined in sql_queries.py, this file is imported into etl.py file to execute the defined SQL queries. Database sparkifydb and above metioned tables are created and dropped using create_tables.py

The etl.py file defines the Extract, Transform and Load process and populates the fact and dimention tables. The **songs** and **artists** tables are populated from songs metadata JSON file residing in **data/song_data** directory and the **users** and **time** tables populated from user log files, **data/log_data**.