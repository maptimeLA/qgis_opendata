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
 * QGIS has the ability to load up ESRI mapserver data, like raster tiles and vector tiles, here's how you can add it.
   * Let's go to the [LACOUNTY Public Server](http://public.gis.lacounty.gov/public/rest/services) | Here you can load raster and vector data onto QGIS
   * To load up raster data, let's pick the aerial imagery, `http://public.gis.lacounty.gov/public/rest/services/LACounty_Cache/LACounty_Aerial/MapServer`
   * On QGIS load up the Python Console in the menu above, under `Plugins`
   * ![Python Console](/images/qgis_raster_1.PNG)
   

 

