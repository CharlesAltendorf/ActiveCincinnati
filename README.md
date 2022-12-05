# Active Cincinnati
Welcome to the Active Cincinnati Github Repository.

## Overview
When the 2020 Census data was released, I was suprised to notice that certain cities had grown after years of population decline.  One of those was Cincinnati.  I went to high school on the Kentucky side of the Ohio River in Florence.  Florence's population has been growing quickly for as long as Cincinnati's has been declining.  So I was curious what kind of factors would bring people back to Cincinnati.  After reviewing the Census Tract data to find where the population had been growing, I wondered if recreation was a factor.  That is when I stumbled across the parks layer that I used to filter out private athletic clubs.

## Methods

### 1_Sources:
    In this folder are source shapefiles and tables that were manipulated in QGIS to Geojsons to be uploaded into mapbox.
#### Cincinnati_City_Boundary:
 Cincinnati City Boundary Shapefile downloaded from CAGIS Open Data Portal. https://data-cagisportal.opendata.arcgis.com/datasets/cincinnati-city-boundary/explore
#### Cincinnati Census Tracts:
This table was constructed after the tiger census tract boundaries were clipped by the Cincinnati City Boundary Shapefile in QGIS.  It contains the 2010 and 2020 populations for each tract, as well as the differences in those populations by number of persons and percentage.  This table was then joined to a clip of the census tiger tracts to create the final CincinnatiCensusTracts20102020 GeoJSON.  The numbers for the table were obtained from Cincinnati Enquirer Data Central 2020 Census Hub.  Although one could probably navigate down to a unique census tract using the parent directory, it was simpler to just use an existing tract and change the tract number as needed.  https://data.cincinnati.com/census/housing/total-population-change/census_tract_30_hamilton_county_ohio/140-39061003000/
#### Countywide_Parks_%26_Green_Spaces: 
Parks and Greenspaces in the Greater Cincinnati Area. This data is odd in some ways because it calls it "county wide" but it included several entries outside of Hamilton County, Ohio.  It also threw geometry errors when attempts were made to clip it in QGIS.  However, applying the filter "PARKTYPE" = 'Clubs-Members Only' OR "PARKTYPE" = 'Clubs-Members Only!' yielded some rather interesting results.
#### tlgdb_2022_a_39_oh.gdb: 
Ohio Census Tract Geodatabase Downloaded from Census Tiger Directory. https://www2.census.gov/geo/tiger/TGRGDB22/
### 2_GeoJSONs:
    These are the final GeoJSONs that were uploaded into Mapbox. They were exported from QGIS into ESPG:4326.
    It should be noted that CincinnatiCensusTracts20102020 didn't inlcude Census Tract 275.  Part of this census tract does fall within the corporate limits of Cincinnati, however such a large area does not it would be impossible to determine where the Cincinnati population lies within it.  
### 3.MapboxScreenshots:
    This folder contains screenshots of some important settings that were used in mapbox.
### 4_HTML:
    These are the final HTML output files that were created.  Code was edited to include mapbox frame with zoom navigation bar.

## Conclusion:
I had fun creating this project and finding one avenue to explore in an effort to explain this phenomenon.  I understand that there may be several other datasets to explore.  I encourage anyone to reach out to me for other ideas.
Thanks,
Charles Altendorf