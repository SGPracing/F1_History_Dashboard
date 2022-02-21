# F1 History Dashboard #

Immerse yourself in the statistics of the history of Formula 1. Get to know the tracks, drivers and teams throughout the seasons. <br/>
Application available at: https://public.tableau.com/app/profile/sergio.pasian/viz/F1_histrory_dash_SGP/F1History?publish=yes br/>

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
Several APIs were requested from http://ergast.com/mrd/
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
Initially 7 tables were available in the database, with 3 major branches: drivers, contructors and circuits. To make sure all the data could have some kind of correlation, a new table ('year') was created, resulting in the following diagram:

<img width="920" alt="Screen Shot 2022-02-20 at 7 03 04 PM" src="https://user-images.githubusercontent.com/92320460/154868304-dfe1220a-314f-4651-87a8-63c2652cb3b0.png">

Obs: in the end, the 'pole position' table was not used to any analysis or visualization because the data colected starting in 1994, thus ignoring 43 F1 seasons.

### 2. Data ###
Files (.csv) were created from the DataFrames.

## Tableau ##

### 1. Data Source ###
Given that all data were distributed within 8 different tables, the data source was structured as such:

<img width="1163" alt="Screen Shot 2022-02-20 at 1 14 53 AM" src="https://user-images.githubusercontent.com/92320460/154829418-889c15e2-a340-4922-a9c7-421c3113e20f.png">

### 2. Dashboard Story ###
A total of 9 dashboards were created. Among them, 2 illustratives (introductory and final one) and 7 with interective menus (sliders and dropdowns).<br/>
Each dashboard has navigation buttons located on the top left and right in order to allow the user to scroll thropugh the pages. <br/>
The graphics used in thois project:
* Bar Charts
* Maps
* Bubble Charts
* Treemaps
* Line Charts

Below, some examples:

<img width="1108" alt="Screen Shot 2022-02-20 at 1 34 15 AM" src="https://user-images.githubusercontent.com/92320460/154830098-0de30d97-8a39-4f63-8d7a-30dfb1358bb2.png">

## Author ##
* Sergio G. Pasian: https://github.com/SGPracing
