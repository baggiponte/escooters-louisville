# Analysing Escooters Data in Lousiville

This is an attempt to reproduce an analysis of [Lousville's dockless vehicles open data](https://data.louisvilleky.gov/dataset/dockless-vehicles).

The project is written in Python. Another project on [classificatin algorithms](https://github.com/baggiponte/escooters-louisville-r) was developed using R.

## Structure of the repo

`rawdata/` contains the raw data, while `data/` contains the cleaned data. Folders are numbered to match the steps of the analysis.

- In `01-data-cleaning` I collected the scripts for cleaning the data. Notably, I used [`geopandas`](https://geopandas.org/) to intersect each observation with a shapefile of the city and obtain start and end neighborhoods for each trip.

## To do list

- Exploratory Data Analysis [EDA]:
    - Fit new distributions and find the better match
    - Improve the analysis of `TripsDistance`
    - Plot the distributions of `ShortTrip == 0` vs `ShortTrip == 1` and test for their differences!
- Time Series:
    - Do a proper TS decomposition and analyse the data with Statsmodels
    - Compare the results of Statsmodels and Prophet
    - Much more if the geospatial analysis is done!
- Geospatial analysis:
    - Learn GeoPandas, load the shapefile and intersect it with the data to filter observations which are out of bounds.
    - Who knows!
- Classification:
    - Implement some classifications models to classify the neighborhood of origin/destination given the data

The real bulk of the project will be the time series analysis (TSA).
