# Sparkify
#### (Data Modeling with Cassandra)
---

Sparkify company wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

The need is for data engineering to be done with an Apache Cassandra database that can create queries on song play data to answer the questions. Here a new database has been created for  this analysis. Test on this database can be done by running queries provided from the analytics team from Sparkify to create the results.


Here Apache Cassandra is used to complete an ETL pipeline using Python. Modeling of the data  is done by creating tables in Apache Cassandra to run queries. The ETL pipeline transfers  the data from a set of CSV files within a directory to creating a streamlined CSV file to model and inserts data into Apache Cassandra tables.

## Datasets:
---

**Event_data**

Event data directory of CSV files is partitioned by date. Here are examples of filepaths to two files in the dataset: 
```
event_data/2018-11-08-events.csv 
event_data/2018-11-09-events.csv
```

**Package Items**
#### Includes one Jupyter Notebook file, in which:
- The ```event_datafile_new.csv``` dataset used to create a denormalized dataset
- Data tables are modeled keeping in mind the queries needed to run
- Queries needed to model the data tables
- Load the data into tables in Apache Cassandra and run the queries

**Process steps**

#### Pre-Processing the Files
1. Import Python packages
2. Creating list of filepaths to process original event csv data files
3. Processing the files to create the data file ```event_datafile_new.csv``` that will be used for Apache Casssandra tables

#### Modeling NoSQL Apache Cassandra database
1. Design tables to answer the required queries
2. Apache Cassandra ``KEYSPACE`` and ```CREATED and SET```
3. Data Tables ```CREATED ```
4. Data loaded with ```INSERTS``` for each of the tables
5. ```IF NOT EXISTS``` and ```DROP``` maintained for reuse and test of ETL pipelines
6. Check table loads with ```SELECTS```

### ETL Pipeline
1. Part I shows logic implemented in iterations through each event file in event_data to process and create a new CSV file in Python
2. Part II includes Apache Cassandra tables created and processed records loaded into relevant tables. Data model verified by running SELECT statements after running the queries on the database.



