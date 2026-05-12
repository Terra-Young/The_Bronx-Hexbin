# Bronx Traffic Collision Hotspot Analysis

## The Spatial Problem
High traffic volume naturally leads to more accidents, but raw collision counts often mask systemic infrastructure failures. This project aims to move beyond simple point mapping to identify statistically significant danger zones in The Bronx, isolating areas where road design and urban layout create disproportionate risk for commuters and pedestrians.

## Analytical Approach
To identify true infrastructure strain, I engineered a spatial autocorrelation model using NYC Open Data (2024 to 2025).
* **Data Aggregation:** Filtered and projected over a year of motor vehicle collision data (EPSG:2263), aggregating the points into a continuous 820 foot hexagonal grid.
* **Spatial Statistics:** Executed a Getis-Ord Gi* analysis using Queen's contiguity to calculate spatial lag. 
* **Significance Filtering:** Applied strict confidence intervals (90%, 95%, and 99%) to filter out random statistical noise, visualizing only areas with proven, significant density clustering.

## Key Insights & Recommendations
* **The Expressways Divide:** Severe, 99% confidence hotspots tightly mirror the South and West Bronx corridors, heavily influenced by the Cross Bronx Expressway and commercial zoning.
* **Residential Coldspots:** The Eastern Bronx presents as a distinct statistical coldspot, correlating with larger residential buffers and major green spaces.
* **Urban Planning Recommendation:** Future municipal interventions, such as traffic calming measures or pedestrian islands, should be heavily prioritized in the identified western hexbins rather than distributed evenly across the borough. 

## Tools Used
* **QGIS:** Geometry creation, spatial statistics, rule-based cartographic rendering.
* **Leaflet / qgis2web:** HTML/JS interactive web map deployment.
* **NYC Open Data:** Motor Vehicle Collisions and LION Street networks.

## Explore the Map
[Insert Link to your Web Map Here]
