## cleanup-trace.py

```python cleanup-trace.py raw-vector-map.geojson```

* reads in a traced GeoJSON file
* removes squares (since these are usually little squares along the lines in the trace)
* removes holes in polygons (since these are usually numbers and text inside of parcels)
* outputs trace-clean-tmp.geojson with these fixes
* if you have GDAL installed on command line, ogr2ogr outputs square.shp folder with these fixes

Not sure if you have GDAL installed? In commmand line / terminal try running ```ogr2ogr```

## georeference.py

```python georeference.py square.kml original.png```

* reads the geo bounds from a KML/KMZ file
* applies them to a PNG or TIF
* uses gdal_translate command to save as a GeoTIFF
