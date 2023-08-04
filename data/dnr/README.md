# DNR Source Data

## Tabular Datasets

- [DNR-FFLIGHT-Export.xlsx](./DNR-FFLIGHT-Export.xlsx)
- [DNR-FFLIGHT-Export.csv](./DNR-FFLIGHT-Export.csv)

and the latest 2023 data:

- [DNR-Latest-Pheasant-Stocking-Properties.xlsx](./DNR-Latest-Pheasant-Stocking-Properties.xlsx)

## GeoJSON

The [GeoJSON](./GeoJSON/) directory contains converted `.geojson` and `.json` files that contain geographic shape/feature polygon data by property.

- [Pheasant-Stocking.geojson](./GeoJSON/Pheasant-Stocking.geojson)
- [Pheasant-Stocking.map.json](./GeoJSON/Pheasant-Stocking.map.json)
- [Pheasant-Stocking.kgl.html](./GeoJSON/Pheasant-Stocking.kgl.html)
- [Log.txt](./GeoJSON/Log.txt)

## Shapefile Archive

[`DNR-FFLIGHT-Export.zip`](./DNR-FFLIGHT-Export.zip): Exported Shapefile `.zip` archive from the DNR's interactive [FFLIGHT](https://dnr.wisconsin.gov/topic/Lands/FFLIGHT.html) application.

- The *Shape File Archive* (also known as `Ersi Shapefile`) as a Zip Archive including files for the following:
  - `.SHP`: (Binary) Feature Geometry Shape File
  - `.SHX`: (Binary) Shape Index Position File
  - `.DBF`: dBase Attribute Metadata Table
  - `.PRJ`: Projection System Metadata (like `XML`)
  - `.CPG`: Configuration file specifying the character set (i.e. `UTF-8`) to be used when displaying text in shapefiles.

See below for an example unzipped export archive from the `FFLIGHT` application:

<center>
  
![image](https://github.com/lakecountryhuntclub/pheasant-stocking-locations-map/assets/32652297/da44c179-8bc0-4fca-a39c-135e6c9565a0)

</center>
