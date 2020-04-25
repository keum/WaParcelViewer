# WaParcelViewer

Summary Diagram of workflow - to be added later
WA Parcel Viewer.jpg

WA state parcel web viewer using WA state geo opendata portal
- This project will describe the data source and steps creating web viewer using following techonlogy
  - WA State Open Data Portal as data source [WA Parcel and Legal Boundaries](http://geo.wa.gov/datasets/wadnr::wa-parcel-and-legal-boundaries)
- QGIS to convert Geodatebase(GDB) to shape file & modify to generate WebLink column
- Use [Tippecanoe](https://github.com/mapbox/tippecanoe) to create mbtiles (vector tiles)
- Use [Tileserver-gl-light](https://www.npmjs.com/package/tileserver-gl-light) simple tileserver tool to serve up converted mbtiles which will be used in Maptunik below for styling.
- [Maptunik](https://maputnik.github.io/) tool to stylize vector tiles and export into style json file that will be used in web map
-
  
