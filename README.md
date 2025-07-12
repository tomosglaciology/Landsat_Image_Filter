
# 🌍 Landsat Image Filter

This repository contains a Google Earth Engine (GEE) script to filter, visualise, and batch download Landsat 4-9 multispectral satellite imagery over a specific area and time range.

## 📦 Features

- ✅ Filters Landsat 4 to 9 imagery by:
  - Date range (Years, Months, Days)
  - CLOUD_COVER
  - CLOUD_COVER_LAND
  - WRS path/row
- ✅ Renaming bands across different Landsat sensors 
- ✅ Displays false-color composite for quick visualisation
- ✅ Exports filtered images in bulk to Google Drive using `geetools` produced by - https://github.com/fitoprincipe/geetools-code-editor/blob/master/batch

## 🛠 Requirements

- [Google Earth Engine](https://earthengine.google.com/) account
- Enable the following Earth Engine user modules:
  - `users/tomosdanielmorgan/EarthObservation:Landsats`
  - `users/fitoprincipe/geetools:batch
- A defined `geometry` variable (either drawn or coded in GEE).
- Optional: A defined WRS path/row.

## 🚀 Usage

1. Open [Google Earth Engine Code Editor](https://code.earthengine.google.com/)
2. Paste the contents of `landsat_example` into a new script.
3. Define your area of interest (AOI) by setting a `geometry` variable.
4. Change data filter and WRS path/row to your AOI.
