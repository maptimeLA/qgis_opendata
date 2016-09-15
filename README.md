# It's a QGIS | Opendata Workshop!

This is a quick breakdown of QGIS and Opendata

###Tools
* QGIS | Opensource Geographic Information System | [Win64](http://qgis.org/downloads/QGIS-OSGeo4W-2.16.2-3-Setup-x86_64.exe) | [Mac](http://www.kyngchaos.com/software/qgis)
 * Note: Windows users have one file to download and install. Mac users have a package to download and need to install additional modules (files) for QGIS to run.

###Explorations

QGIS plugins for exploring data
 * OpenLayers | Allows you to load tiles for baselayers | Options include OpenStreetMap, Google Maps, Bing Maps, Mapquest, Stamen and Apple Maps
 * OSM Place Search | Address and Place geocoder to move the map to that requested location | Great if you want to zoom to a particular location
 * qgis2web | This generates a webmap of your project in OpenLayers or Leaflet
 * Qgis2threejs | Makes a 3D model of your project for the web | See it in 3D!
 
Opendata portals to explore
 * [City of Los Angeles Data Portal](https://data.lacity.org/)
 * [City of Los Angeles GeoHUB portal](https://geohub.lacity.org/)
 * [LA County Data Portal](data.lacounty.gov)
 * [LA County GIS Data Portal](http://egis3.lacounty.gov/dataportal/)
 * [ESRI Open Data Portal](http://opendata.arcgis.com/)
 * [Vyki's List of Datasources](https://github.com/vykster/los-angeles-data-sources) | [Find her at HackforLA!](http://www.hackforla.org/)

Smooth move, maptimer (Tricks and tips)
 * QGIS has the ability to load up ESRI mapserver data, like raster tiles and vector tiles, here's how you can add it. [Link to detailed steps](https://hub.qgis.org/wiki/17/Arcgis_rest)
   * Let's go to the [LACOUNTY Public Server](http://public.gis.lacounty.gov/public/rest/services) | Here you can load raster and vector data onto QGIS
   * To load up raster data, let's pick the aerial imagery, `http://public.gis.lacounty.gov/public/rest/services/LACounty_Cache/LACounty_Aerial/MapServer`
   * On QGIS load up the Python Console in the menu above, under `Plugins`
   * ![Python Console](/images/qgis_raster_1.PNG)
   * In the console copy and paste this into the triple arrow area `qgis.utils.iface.addRasterLayer("[insert your mapserver URL here]?f=json&pretty=true","raster")` | Replace the `insert your mapserver URL here` with the link above or any other link you may find and hit enter.
   * Depending on your zoom level, you may need to adjust your extents (the area where the data is located) and zoom there. In this case the county aerial imagery is only LA County. You would need to zoom there or use the OSM Place search to quickly take you there.
   
* Using spreadsheet prgms like Excel or Google Sheets to split a column with both Lat and Long into two columns for loading into QGIS
 * We can use this dataset to download a CSV file, [`https://data.lacity.org/A-Prosperous-City/Pizza-Locations/66es-k6kk`](https://data.lacity.org/A-Prosperous-City/Pizza-Locations/66es-k6kk)
 * Download the CSV and load it into Google Sheets
 * In Google Sheets you need to add the Power Tools Add-on, goto the Add-ons tab and select Get Add-ons, search and install.
 * First step is to remove all the parentheses in the column
   * Hit CTRL-H or Edit --> Find and Replace to pull the Find and Replace window
   * In the `Find` type the ` ( ` and in the `Replace with` leave it blank | This will remove the parentheses
   * Repeat the same step with the ` ) ` | Once both parentheses are removed we can split the column by the comma in between
   * With the column selected, run the Power Tools Add-on and select Split | This will open a window with options to split by space, line break, comma etc | Choose the comma and hit split
   * This should split the column into two, now we can delete the column with both Lat and Lon and download the CSV file for loading onto QGIS.
   
   
   

 

