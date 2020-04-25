## Summary Diagram of workflow - to be added later
WA Parcel Viewer.jpg

## WA state parcel web viewer using WA state geo opendata portal
Below describes the data source and steps to create web viewer using following stack of open source technology.
  ### Data Collect
  - WA State Open Data Portal as data source [WA Parcel and Legal Boundaries](http://geo.wa.gov/datasets/wadnr::wa-parcel-and-legal-boundaries)
### Data Convert 
- QGIS to convert Geodatebase(GDB) to shape file & modify to generate WebLink column
- Use [Tippecanoe](https://github.com/mapbox/tippecanoe) to create mbtiles (vector tiles)

### Data Assemble
- Use [Tileserver-gl-light](https://www.npmjs.com/package/tileserver-gl-light) simple tileserver tool to serve up converted mbtiles which will be used in Maptunik below for styling.
- [Maptunik](https://maputnik.github.io/) tool to stylize vector tiles and export into style json file that will be used in web map

### Create Web Map
- Used [Mapbox Web-gl-js](https://docs.mapbox.com/mapbox-gl-js/api/)to assemble web map
- Used [Mapbox gl-inspect](https://www.npmjs.com/package/mapbox-gl-inspect) tool to identify clickable selected individual parcel
- Used [Mapbox gl-geocode](https://docs.mapbox.com/mapbox-gl-js/example/mapbox-gl-geocoder/)  
- One can use [bl.ocks.org](https://bl.ocks.org/-/about) tool to test web map and deploy 
