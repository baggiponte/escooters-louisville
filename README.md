# Analysing Escooters Data in Lousiville

## Premise

This is an attempt to replicate and expand the analysis of [Lousville's dockless vehicles open data](https://data.louisvilleky.gov/dataset/dockless-vehicles) that I went through with Aldo, Aleksei and Maria Grazia. Kudos to you for this experience together! You can find the original project stored in [this Google Drive folder](https://drive.google.com/drive/folders/1cWw1EG64_ijIEVZGLwZEs3UK0ek6cO6O?usp=sharing).

The project is written in Python. Another project on [classificatin algorithms](https://github.com/baggiponte/escooters-louisville-r) was developed using R and can be viewed via [this blog](https://louisville-dockless-vehicles.rbind.io/), built with [Netlify](https://www.netlify.com/) and [Blogdown](https://bookdown.org/yihui/blogdown/). The code for the blog is also stored in [this GitHub repo](https://github.com/baggiponte/blogdown-escooters-louisville-r).

## Structure of the repo

`rawdata/` contains the raw data, while `data/` contains the cleaned data. Folders are numbered to match the steps of the analysis.

- In `01-data-cleaning` I collected the scripts for cleaning the data. Notably, I used [`geopandas`](https://geopandas.org/) to intersect each observation with a shapefile of the city and obtain start and end neighborhoods for each trip.

## To do list

- Exploratory data analysis:
    - Fit more distributions and find the better match
    - Plot the distributions of `ShortTrip == 0` vs `ShortTrip == 1` and test for their differences!
- Time series:
    - Do a proper TS decomposition and analyse the data with Statsmodels
    - Compare the results of Statsmodels and Prophet
- Geospatial analysis  and (more) classification:
    - Create a n by n grid to assign each trip to and perform classification using each cell.
