# Pheasant Locations Geographic Map Data

> **Note** Original data is sources from the [Department of Natural Resources (DNR) of Wisconsin](https://dnr.wisconsin.gov/).

## Contents

- [Latest Locations Table](#latest-locations-table)
- [Geographic Data from the FFLIGHT App](#geographic-data-from-the-fflight-app)
  - [GeoJSON](#geojson)
  - [Shapefile Archive](#shapefile-archive)
  - [Tabular CSV and Excel Data](#tabular-csv-and-excel-data)
 - [ArcGIS Data](#arcgis-data)

## Latest Locations Table

- See the DNR's [2023 Pheasant Stocking Homepage](https://apps.dnr.wi.gov/pheasantstocking/Index.aspx):
  - To view the latest dataset table, scroll to the bottom of the page and hit the "Search" button. This will display the latest listing of properties and their attributes (with the option to export to Excel) like below: 

<center>
  
![image](https://github.com/lakecountryhuntclub/pheasant-stocking-locations-map/assets/32652297/691fb999-2565-47ec-a7c5-c69cb52994e8)

</center>


## Geographic Data from the FFLIGHT App

Besides basic location information from the table above, we also need Geographic (`GIS`) data for the properties with data representing their Geometry (GeoData) and Shapes.

- This data was collected by interacting with the [FFLIGHT](https://dnr.wisconsin.gov/topic/Lands/FFLIGHT.html) application, selecting the Pheasant Stocking Layer and exporting each property's data.
- Each location has a corresponding "Geometry" or "Shape" represented as a map layer of polygons, specifically the data is *GeoCortex.GIS.Geometries.Polygon* format per location.

Using the DNR's [FFLIGHT](https://dnr.wisconsin.gov/topic/Lands/FFLIGHT.html) application, you can interact and export individual property geographic data in various formats such as:

- Comma-Separated Values (`CSV`)
- Excel (`.xlsx`)
- GeoJSON (`geojson` or `json`)
- Shapefile Archive (`.zip`, see below for details)  

### GeoJSON 

**Geographic JavaScript Object Notation (GeoJSON)**: The GeoJSON format is mostly for web-based mapping.
    -   File Extensions:
        -   `.GEOJSON`
        -   `.JSON`
    -   GeoJSON stores coordinate as text in JavaScript Object Notation (JSON) form. 
    -   This includes vector points, lines and polygons as well as tabular information. GeoJSON store objects within curly braces {} and in general have less markup overhead (compared to GML).
    -   GeoJSON has a straightforward syntax that you can modify in any text editor. 
    -   Webmaps browsers understand JavaScript so by default GeoJSON is a common web format. But JavaScript only understands binary objects. Fortunately, JavaScript can convert JSON to binary.

Example GeoJSON by Feature:

<center>

![image](https://github.com/lakecountryhuntclub/pheasant-stocking-locations-map/assets/32652297/360583a3-6ea6-4b44-9e1d-f7d1c3b59a8d)

</center>

<details><summary>View Example JSON</summary><p>

```json
{
    "type": "FeatureCollection",
    "name": "merged",
    "features": [
        {
            "type": "Feature",
            "properties": {
                "OBJECTID": 93740,
                "LMS_LOCAL_": 9493,
                "PROP_NAME": "SAUK PRAIRIE RECREATION AREA",
                "MAP_VISIBL": "Y",
                "STOCKING_Y": "2022",
                "ACRES_SUIT": 1000,
                "PROPOSED_S": 640,
                "MAX_BIRDS_": 100,
                "SHAPE_AREA": 4473445.1447146898,
                "SHAPE_LEN": 11418.340495075799
            },
            "geometry": {
                "type": "Polygon",
                "coordinates": [
                    [
                        [
                            543464.28870000038296,
                            322248.674499999731779
                        ],
                        [
                            543564.872899999842048,
                            322131.32630000077188
                        ],
                        [
                            543849.861499999649823,
                            321594.877199999988
                        ],
                        [
                            542760.199300000444055,
                            321653.551300000399351
                        ],
                        [
                            542768.581299999728799,
                            321041.664100000634789
                        ],
                        [
                            542701.5252,
                            321058.42820000089705
                        ],
                        [
                            542726.671299999579787,
                            320723.14750000089407
                        ],
                        [
                            543506.198800000362098,
                            320689.619400000199676
                        ],
                        [
                            543514.580799999646842,
                            319809.507699999958
                        ],
                        [
                            541335.25650000013411,
                            319809.507699999958
                        ],
                        [
                            541343.638500000350177,
                            320815.349700000137091
                        ],
                        [
                            541243.0543,
                            321033.282099999487
                        ],
                        [
                            541553.188900000415742,
                            321041.664100000634789
                        ],
                        [
                            541553.188900000415742,
                            322282.202600000426173
                        ],
                        [
                            543464.28870000038296,
                            322248.674499999731779
                        ]
                    ]
                ]
            }
        },
        // ... etc.
````

</p></details>

### Shapefile Archive

The *Shape File Archive* (also known as `Ersi Shapefile`) as a Zip Archive including files for the following:
  - `.SHP`: (Binary) Feature Geometry Shape File
  - `.SHX`: (Binary) Shape Index Position File
  - `.DBF`: dBase Attribute Metadata Table
  - `.PRJ`: Projection System Metadata (like `XML`)
  - `.CPG`: Configuration file specifying the character set (i.e. `UTF-8`) to be used when displaying text in shapefiles.

See below for an example unzipped export archive from the `FFLIGHT` application:

<center>
  
![image](https://github.com/lakecountryhuntclub/pheasant-stocking-locations-map/assets/32652297/da44c179-8bc0-4fca-a39c-135e6c9565a0)

</center>

### Tabular CSV and Excel Data

- See the exported CSV: [DNR-FFLIGHT-Export.csv](./dnr/DNR-FFLIGHT-Export.csv)
- See the exported Excel Workbook: [DNR-FFLIGHT-Export.xlsx](./dnr/DNR-FFLIGHT-Export.xlsx)

These tables include similar fields to the data from the DNR's [Latest Locations Table](#latest-locations-table), but not updated for 2023 yet.

Specifically the fields are:

- `geometry`
- `OBJECTID`
- `SHAPE`
- `LMS_LOCAL_PROP_ID`
- `PROP_NAME`
- `MAP_VISIBLE_FLAG`
- `STOCKING_YEAR`
- `ACRES_SUITABLE_HUNTING`
- `PREVIOUS_STOCKING_LEVEL`
- `PROPOSED_STOCKING_LEVEL`
- `MAX_BIRDS_PER_STOCKING`
- `COMMENTS_TEXT`
- `SHAPE.AREA`
- `SHAPE.LEN`

## ArcGIS Data

- [ ] TODO



