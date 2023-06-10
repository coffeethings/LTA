### Visualising consumed data from LTA APIs

#### Purpose
Collect the road incidents data and road traffic bands data from LTA's two different Application Programming Interface (API).

#### Steps
* First gather the traffic incident data:
  * Create a Python programme requesting for the data using URL and get the return JSON data.
  * Extract and format the JSON traffic incident data into a Pandas dataframe.

* Similarly for the traffic band data:
  * Create a Python programme to request for the data using its corresponding URL and get the return JSON data. 
  * Extract and format the JSON traffic band data into a Pandas dataframe.

* Finally, visualise all the collected data on a map with various clickable location markers that will display the corresponding information by utilising Python's Folium library.

#### Problem encountered
The Singapore map with the different location markers cannot be displayed when using Folium despite different attempts at coding.

Some alternative ways used to map the coordinates for the location markers include:
* Plotly, an interactive, open-source, and browser-based graphing library for Python;
* The use of shapefile, a file format for geospatial data:
  * First a shapefile of Singapore is downloaded from Data.gov.sg.
  * Next, the Coordinate Reference Systems (CRS) is set to EPSG: 4326 for WGS 84, a commonly used geodetic system [1, 2].
  * Then, a Singapore map is plotted.
  * Following that, the latitudes and longitudes are turned into geometry points.
  * Finally, these points are plotted onto the Singapore map.

#### Future improvement
Run the notebook again on a cloud platform such as Google Collaboratory to determine if the marker display issue is local. There could be some system compatibility issues as the Jupyter notebook was run locally.

#### References
[1] GeoPandas, “Managing projections — Coordinate Reference Systems,” Geopandas.org. [Online]. Available at: https://geopandas.org/en/stable/docs/user_guide/projections.html. [Accessed: July 9, 2022].

[2] “EPSG:4326,” epsg.io. [Online]. Available at: https://epsg.io/4326. [Accessed: July 9, 2022].

Singapore shape file is obtained from here:
https://data.gov.sg/dataset/master-plan-2014-land-use?resource_id=0d1a6cda-7cad-4b17-b9a8-9e173afebbc1
