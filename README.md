# Project Description

This repo is for Jack Bienvenue's BS in Statistical Data Science Capstone Project. The research project focuses on evaluating changes in property values in coastal and non-coastal regions of the United States with an interest in coastal pricing acceleration acting in opposition to climate change driven or accentuated risk factors.

![](images/house.gif)


[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/j3A4H7fc)

# Analysis Steps

## Data Download

### Zillow Data

Zillow data for home valuations is accessible via [NASDAQ Data Link](https://www.nasdaq.com/solutions/data/nasdaq-data-link). Access is free for Zillow data, but requires registering for an account. 

### Shapefiles 

The shapefiles used to construct the coastal and non-coastal shapefiles, and later the datasets of coastal and non-coastal properties, were sourced in the following way:

#### US Counties

The shapefile for US counties used in this analysis can be found [here](), provided by WHO

#### US Zip Codes

The shapefile for US zip codes used in this analysis can be found [here](), provided by WHAT

#### US neighborhoods

The shapefile for US Zillow neighborhoods used in this analysis has been published by the EPA and can be found here. 

## Pre-Processing Outside Repo

### Creation of coastal/ non-coastal shapefile

The coastal/ non-coastal shapefiles are fundamental to the methods for this analysis.

These shapefiles were constructed in ArcGIS Pro in the following manner:

- US Counties
    - Coastal
        - Manual selection of counties abutting the Atlantic and Pacific Oceans, as well as the Great Lakes.
    - Non-Coastal
        - Inverse selection of county dataset, exlcuding coastal counties.
- US Zip Codes
    - Coastal
        - Inclusion of all zip codes which intersect the coastal counties. 
    - Non-Coastal
        - Inverse selection of newly created coastal zip code dataset.
- US Neighborhoods
    - Coastal
        - Inclusion of all neighborhoods which intersect the coastal counties
    - Non-Coastal
        - Inverse selection of newly created coastal zip code dataset.

In this way, there is consistency in the definition of land areas included in the coastal dataset. Since zip codes and neighborhoods are typically smaller than counties (in localized areas), defining them as those which abut the coast would lead to a smaller area of inclusion for zip code and neighborhood-listed properties.

## Data Subset Selection

When selecting a subset for the data, it is important to note that we want to ensure both spatial and temporal diversity. Spatial diversity's importance is twofold: first, we want to ensure that different areas of the United States's coast and inland area is represented and second, we want to ensure that both the coastal and non-coastal sets are well-populatied. Temporally, we know that our available data ranges from 01/31/1996 to 08/03/2024. This does not mean that the data available within this time range is uniform spatiotemporally. 

## Data Cleaning

### Localization

### Coastal & Non-Coastal Sample Assembly


