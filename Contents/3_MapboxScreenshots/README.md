# ActiveCincinnati
Welcome to the Active Cincinnati Github Repository.
This directory contains 4 folders:

1.GeoJSONs:
    These are the final GeoJSONs that were uploaded into Mapbox. They were exported from QGIS into ESPG:4326.
    It should be noted that CincinnatiCensusTracts20102020 didn't inlcude Census Tract 275.  Part of this census tract does fall within the corporate limits of Cincinnati, however such a large area does not it would be impossible to determine where the Cincinnati population lies within it.  
    It should also be noted that centriods and filters were unable to be executed on the Private Athletic Clubs data due to invalid geomtry erros QGIS kept throwing.

2.HTML:
    These are the final HTML output files that were created.  Code was edited to include mapbox frame with zoom navigation bar.

3.MapboxScreenshots:
    This folder contains screenshots of some important settings that were used in mapbox.

4.Sources:
    In this folder are source shapefiles and tables that were manipulated in QGIS to Geojsons to be uploaded into mapbox.
    Cincinnati_City_Boundary: Cincinnati City Boundary Shapefile downloaded from CAGIS Open Data Portal. https://data-cagisportal.opendata.arcgis.com/datasets/cincinnati-city-boundary/explore
    Cincinnati Census Tracts: This table was constructed after the tiger census tract boundaries were clipped by the Cincinnati City Boundary Shapefile in QGIS.  It contains the 2010 and 2020 populations for each tract, as well as the differences in those populations by number of persons and percentage.  This table was then joined to a clip of the census tiger tracts to create the final CincinnatiCensusTracts20102020 GeoJSON.  The numbers for the table were obtained from Cincinnati Enquirer Data Central 2020 Census Hub.  Although one could probably navigate down to a unique census tract using the parent directory, it was simpler to just use an existing tract and change the tract number as needed.  https://data.cincinnati.com/census/housing/total-population-change/census_tract_30_hamilton_county_ohio/140-39061003000/
    Countywide_Parks_%26_Green_Spaces: Parks and Greenspaces in the Greater Cincinnati Area. This data is odd in some ways because it calls it "county wide" but it included several entries outside of Hamilton County, Ohio.  It also threw geometry errors when attempts were made to clip it in QGIS.  However, applying the filter "PARKTYPE" = 'Clubs-Members Only' OR "PARKTYPE" = 'Clubs-Members Only!' yielded some rather interesting results.
    tlgdb_2022_a_39_oh.gdb: Ohio Census Tract Geodatabase Downloaded from Census Tiger Directory. https://www2.census.gov/geo/tiger/TGRGDB22/

Feel free to contact me anytime for comments on my project or other ideas to explore in the future.
Thanks,
Charles Altendorf