
# 🌍 Landsat Image Filter

This repository contains a Google Earth Engine (GEE) script to filter, visualise, and batch download Landsat 4-9 multispectral satellite imagery over a specific area and time range. Co-Developed with [`iamdonovan`](https://github.com/iamdonovan).
 

## 📦 Features

- ✅ Filters Landsat 4–9 imagery by:
  - Date range (start and end year, month, day)
  - Image cloud cover
  - Land cloud cover
  - WRS path and row

- ✅ Renames bands across different Landsat sensors for consistency.

- ✅ Displays both false-color and true-color composites for quick visualization.

- ✅ Exports filtered image collections to Google Drive using [`geetools`](https://github.com/fitoprincipe/geetools-code-editor/blob/master/batch).

## 🛠 Requirements

- [Google Earth Engine](https://earthengine.google.com/) account
- Enable the following Earth Engine user modules:
  - `users/tomosdanielmorgan/EarthObservation:Landsats`
  - `users/fitoprincipe/geetools:batch`
- A defined `geometry` variable (either drawn or uploaded in GEE).
- Optional: A defined WRS path/row.

## 🚀 Usage

1. Open [Google Earth Engine Code Editor](https://code.earthengine.google.com/)
2. Paste the contents of `landsat_example` into a new script.
3. Define your area of interest (AOI) by setting a `geometry` variable.
4. Change data filter and WRS path/row to your AOI.
   
## 🔧 Filtering Options with `funcs`

A summary of the available filtering functions in the custom `funcs` module:

| Function | Description |
|----------|-------------|
| `funcs.allLandsat` | Filters **Landsat 4–9** |
| `funcs.EarlyLandsat` | Filters **Landsat 4, 5, and 7** |
| `funcs.NewLandsat` | Filters **Landsat 8 and 9** |
| `funcs.landsat4` | Filters only **Landsat 4** |
| `funcs.landsat5` | Filters only **Landsat 5** |
| `funcs.landsat7` | Filters only **Landsat 7** |
| `funcs.landsat8` | Filters only **Landsat 8** |
| `funcs.landsat9` | Filters only **Landsat 9** |
