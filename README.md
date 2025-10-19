# Investigating Socioeconmic and Environmental Impacts of Redlining in Los Angeles

### Author: Kylie Newcomer

### 10/18/2025

This repository contains the materials for the exploring patterns of environmental justice homework assignment for **EDS 223 Geospatial Analysis and Remote Sensing**. Materials for this assignment can be found on the [course website](https://eds-223-geospatial.github.io/).

## Data

Environmental justice data is from the United States Environmental Protection Agency's EJScreen: Environmental Justice Screening and Mapping Tool, which is no longer available, but can be downloaded from [this Google Drive link](https://drive.google.com/file/d/1nG6Nj1bXfzQFOVMO8Km3eNy4SWu1YcIQ/view).

Redlining data is based on the  Home Owners' Loan Corporation (HOLC) grading of neighborhoods from 1935 to 1940 and was created by the Digital Scholarship Lab at the University of Richmond through the [Mapping Inequality Project](https://dsl.richmond.edu/panorama/redlining/#loc=5/39.1/-94.58). Data can be downloaded from [this link](https://dsl.richmond.edu/panorama/redlining/data).

Bird observation data is from the Global Biodiversity Information Facility. Only observations from 2021-2023 were used for this analysis.

## Workflow
### Part 1
The data for this project was read in and assigned a CRS using the `st_transform` function to make the visualization process smoother. The EJScreen data was filtered down to only Los Angeles County and an inital map of redlining using the mapping inequity project data was created. The inequity project data had invalid geometry points, so the data was transformed and then joined with the L.A. environmental justice data set to create a summary of population percentages within each grade. The highest percentage of the population was in grade C - "Definitely Declining", followed by D - "Hazardous" then B - "Still Desirable" and finally A - "Best".

Data was summarized to find the average of various environmental and socioeconomic factors by HOLC grade. The mean percent of low income households was highest in the D "Hazardous" neighborhoods, while the least percent of low income households was in the A "Best" neighborhoods. Similarly, the percentile of low life expectancy and particulate matter 2.5 was highest in the D "Hazardous" neighborhoods and decreased as neighborhood grade increased. These results support the claims that red lining has disproportionately impacted underpriveledged groups.

### Part 2
To analyze the impacts of redlining on bird observations from 2021-23, the bird data was first filtered to the 
years of interested. The bird and redlining data was combined to to include only bird observations within a HOLC graded neighborhood. When summarizing the proportion of observations by HOLC grade, C neighborhoods had the highest percent of observations, followed by A and D neighborhoods. These results are not the same as the Ellis-Soto et al. 2023 study.

## References

Cartier, K. M. S. (2023), Bird biodiversity reports reflect cities’ redlined past, Eos, 104, https://doi.org/10.1029/2023EO230375. Published on 5 October 2023. Date Accessed: Oct 18, 2025 

Nelson, Robert K., LaDale Winling, et al. “Mapping Inequality: Redlining in New Deal America.” Edited by Robert K. Nelson, American Panorama: An Atlas of United States History, 2023. Date Accessed: Oct 18, 2025
dsl.richmond.edu/panorama/redlining

United States Environmental Protection Agency. 2015. EJSCREEN. Date Accessed: Oct 6, 2025 <https://19january2017snapshot.epa.gov/ejscreen/frequent-questions-about-ejscreen_.html>