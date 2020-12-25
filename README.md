# Analysing Escooters Data in Lousiville

This is an attempt to analyse and mine the open data of the usage of the dockless vehicles in Louisville. I will update the `README` with every new step of the analysis.

The project is run with Python. There will be some other extensions with other programming languages, notably and very soon in R.

This also happens to be my true first repo, yay!

## Structure of the repo

`rawdata/` contains the raw data, while `data/` contains the tidied and modified data. Folders are numbered to match the steps of the analysis.

## To do list

- Add the sources
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
