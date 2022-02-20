# F1 History Dashboard #

Immerse yourself in the statistics of the hostory of Formula 1. Get to know the tracks, drivers and teams throughout the seasons. <br/>

## Data ##
Source: http://ergast.com/mrd/

## Technology ##
* Python 3.9.7
* PostgreSQL
* Tableau Public

## Python ##

### 1. Libraries ###
* requests
* pandas
* numpy
* sqlalchemy
* dotenv
* os

### 2. Requestiong API ###
In total, 5 APIs were requested from http://ergast.com/mrd/:
* Constructor Standings
* Driver Standings
* qualifying
* circuits

### 3. DataFrames ###
Subsequently 7 dataframes were created from the requested APIs, as such:

<img width="873" alt="Screen Shot 2022-02-20 at 12 54 44 AM" src="https://user-images.githubusercontent.com/92320460/154828967-50c68ed6-a3fc-4a8a-bd42-2d4ff9716fc8.png">

### 4. Exporting DataFrames ###
All dataframes were exported to a SQL database in PostgreSQL. <br/>
Dotenv was used to mask user and password.<br/>

## SQL ##

### 1. ERD ###
Initially 7 tables were available in the database, with 3 major branches: drivers, contructors and circuits. To make sure all the data could have some kind o correlation, a new table ('year') was created, resulting in this diagram:

<img width="874" alt="Screen Shot 2022-02-20 at 1 09 58 AM" src="https://user-images.githubusercontent.com/92320460/154829280-fba820aa-ac8e-4b27-9b7b-64c056ac62f3.png">

### 2. Data ###
All tables were then exported as .csv files.

## Tableau ##

### Data Source ###
Given that all data were distributed within 8 different table, the data source was structured as such:


<img width="1163" alt="Screen Shot 2022-02-20 at 1 14 53 AM" src="https://user-images.githubusercontent.com/92320460/154829418-889c15e2-a340-4922-a9c7-421c3113e20f.png">
