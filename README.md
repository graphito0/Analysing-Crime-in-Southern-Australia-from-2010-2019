# Analysing-Crime-in-Southern-Australia-from-2010-2019

***Using Spark for distributed processing and Mongodb as a database. we will analyse crimes in Southern Australia from 2010 - 2019 and draw some insights through visualisations.***

***The whole idea of the project is to demonstrate that if our data (CVS file) is stored in a database (MongoDB) far away, then through modules (Spark SQL) and distributed processing engine (Spark) we can access the data as well as conduct operations on it.***

## Overview

![diagram](https://user-images.githubusercontent.com/30866240/64483794-3cbede80-d24c-11e9-8e20-6ddfa12890f4.PNG)

1. Spark has the ability for distributed data processing, in the above schematic diagram it acts as a core engine function.
2. Spark SQL is Saprk's module for working with structured data.
3. Data Frame in our case the CSV data on which we will store it in the MongoDB and then access it through Spark on which Spark SQL will perform certain queries.
4. Visualisation is visualising the results generated by the queries.

## Metadata
   - Crime_statistics is in CSV format with approx 700k rows.
   - The file has fields,
   1. Reported Date 
   2. Suburb - Incident 
   3. Postcode
   4. Offence Level 1 Description
   5. Offence Level 2 Description
   6. Offence Level 3 Description
   7. Offence Count
   - All the fields are in string format except Offence Count which is integer
   

## General Steps

  1. Installation 
  - MongoDB and Apache Saprk, previous repository https://github.com/graphito0/Big_Data_Processing/ has steps for installing both of         them.
  - Installation file provides easy steps on installing a virtual environment, jupyter notebook and other dependencies.
  
  2. Processing
    2.1 First we will create Spark Context which serves as a primary entry point and Spark session to define configurations for                 connecting mongoDb.
    2.2 We then read the data as a spark defined dataframe and then store it to MongoDB.
    2.3 After storing, the dataframe is again accessed through MongoDB and queries are executed using Spark SQL functions.
    2.4 The results are then visulaised through matplotlib.
    
## Files
  
  1. Analysing_crime.ipnyb - contains the executions of the processes.
  1. Crime_statistics.csv - Data to be processed.
  2. Specifications.pdf - Contains all the steps in detail and the queries to be executed
  3. Installation.pdf - Contains all the steps for installation of modules and dependencies.
   
