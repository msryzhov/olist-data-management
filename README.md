# olist-data-management
Mission is to help OList structure its data department,
to organise architecture, technologies and data processing.

## Question 1.1
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

## Question 1.2
__Describe a data warehouse schema which would allow you to use as much
information as possible from the Kaggle’s extract you have, while providing you capabilities
to answer marketing department questions.__

Basic Star Schema of Data Warehouse
![DW_star](https://github.com/msryzhov/olist-data-management/blob/main/q_1_2.png)

## Question 1.3
__Describe how you could improve this basic data architecture to address
potential future needs that you think could provide value to the organization.__

First possible improvements is to go to Snowflake schema by breaking down
dimensions tables to get possibilities study reports for example according
product categories and etc.

## Question 2.2
__Imagine and create a segmentation based on the extracted data which will
allow to group customers based on their purchase location.__

You could find detail in ![Geo segmentation report](https://github.com/msryzhov/olist-data-management/blob/main/Geo_segmentation.pdf)
