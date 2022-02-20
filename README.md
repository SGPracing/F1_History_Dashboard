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
Subsequently 7 dataframes were created from the requested data, as such:

<img width="873" alt="Screen Shot 2022-02-20 at 12 54 44 AM" src="https://user-images.githubusercontent.com/92320460/154828967-50c68ed6-a3fc-4a8a-bd42-2d4ff9716fc8.png">
