# olist-data-management
Mission is to help OList structure its data department,
to organise architecture, technologies and data processing.

##Question 1.1
__Describe a basic data architecture which will allow you to gather data and
create at least a data warehouse layer for analytics purposes.
Identify the technologies you
would probably use to implement this first architecture.__

We have 2 main sources of data:
 - Operational database;
 - Google analytics.

 Current goal is to provide data infrastructure to build metrics
 for a Marketing department. We will organize Data Warehouse with a Data Mart
 to make a visibility policy for different actors.

 A simple architecture to achieve this goal is follow:
 (Operational DB) -(ETL)-> (Staging DB) -(ETL)-> (Data Warehouse) -(ETL)->
 (Data Mart) -> Visualization Tool

 Concerning Google analytics data right now we have no particular need to
 use this kind of data, but we need to store it for future needs.
 So, we can use Google Analytics API to retrieve data and store it to
 some NoSQL database.
