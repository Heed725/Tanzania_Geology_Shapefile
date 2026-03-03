# Tanzania Geology Shapefile

A GIS shapefile dataset containing geological map data for Tanzania, suitable for use in QGIS, ArcGIS, and other GIS applications.

[![Download Shapefile](https://img.shields.io/badge/⬇%20Download%20Shapefile-blue?style=for-the-badge)](https://github.com/Heed725/Tanzania_Geology_Shapefile/archive/refs/heads/main.zip)
[![QGIS](https://img.shields.io/badge/QGIS-3.x%20Compatible-green?style=for-the-badge&logo=qgis&logoColor=white)](https://qgis.org)
[![Version](https://img.shields.io/badge/Version-1.0.0-orange?style=for-the-badge)](https://github.com/Heed725/Tanzania_Geology_Shapefile/releases)

## Overview

This repository provides geological spatial data for Tanzania in ESRI Shapefile format. The data covers rock formations, lithological units, and geological structures across the country, making it useful for research, academic study, mineral exploration, environmental assessment, and hydrogeological analysis.

Tanzania's geology is diverse — spanning Precambrian basement rocks, Proterozoic mobile belts, Karoo sedimentary sequences, and Cenozoic rift volcanics associated with the East African Rift System.

## Contents

```
Tanzania_Geology_Shapefile/
├── tanzania_geology.shp       # Main geometry file
├── tanzania_geology.shx       # Shape index file
├── tanzania_geology.dbf       # Attribute data (dBASE format)
├── tanzania_geology.prj       # Coordinate reference system (CRS)
└── README.md
```

> Note: All four files (`.shp`, `.shx`, `.dbf`, `.prj`) are required for the shapefile to function correctly.

## Attributes

The attribute table may include fields such as:

| Field | Description |
|---|---|
| `GEOL_CODE` | Geological unit code |
| `ROCK_TYPE` | Lithological classification (e.g., granite, basalt, sediment) |
| `AGE` | Geological age or era |
| `FORMATION` | Named geological formation |
| `DESCRIPTION` | General description of the unit |

## Coordinate Reference System

- **Projection:** Geographic coordinate system
- **Datum:** WGS 1984
- **EPSG:** 4326

## Usage

### QGIS
1. Open QGIS
2. Go to **Layer → Add Layer → Add Vector Layer**
3. Browse to the `.shp` file and click **Add**

### ArcGIS
1. Open ArcMap or ArcGIS Pro
2. Use **Add Data** and navigate to the `.shp` file

### Python (GeoPandas)
```python
import geopandas as gpd

gdf = gpd.read_file("tanzania_geology.shp")
print(gdf.head())
gdf.plot(column="ROCK_TYPE", legend=True)
```

## Data Sources

Geological data derived from publicly available sources including:
- [Geological Survey of Tanzania (GST)](http://www.gst.go.tz/)
- British Geological Survey (BGS) – Africa Groundwater Atlas
- USGS / Persits et al. (2002) Africa geology dataset

## License

This data is shared for educational and research purposes. Please cite the original geological survey sources when using this dataset in publications or projects.

## Contributing

Pull requests are welcome. If you find errors in the geometry or attributes, please open an issue with details about the discrepancy and the source you are referencing.

## Author

**Heed725**
GitHub: [https://github.com/Heed725](https://github.com/Heed725)
