
# 🌍 Google Earth Engine Landsat 4–9 Filter and Batch Export

This repository contains a Google Earth Engine (GEE) script to filter, visualise, and batch download Landsat 4-9 Collection 2 Tier 1 Top-of-Atmosphere (TOA) multispectral satellite imagery over a defined area and time range. Co-developed with [`iamdonovan`](https://github.com/iamdonovan). Our script uses [`batch`](https://github.com/fitoprincipe/geetools-code-editor/blob/master/batch) produced by [`fitoprincipe`](https://github.com/fitoprincipe).

## 📦 Features

- ✅ Filters Landsat 4–9 imagery by:
  - Date range (start and end year, month, day)
  - Image cloud cover
  - Land cloud cover
  - WRS path and row

- ✅ Renames bands across different Landsat sensors for consistency.

- ✅ Displays both false-color and true-color composites for quick visualisation.

- ✅ Exports filtered Image Collection to Google Drive using [`batch`](https://github.com/fitoprincipe/geetools-code-editor/blob/master/batch).

## 🛠 Requirements

- [Google Earth Engine](https://earthengine.google.com/) account
- Require the following Earth Engine user modules:
  - `users/tomosdanielmorgan/EarthObservation:Landsats`
  - `users/fitoprincipe/geetools:batch`
- A defined `geometry` variable (either drawn or uploaded in GEE).
- Optional: A defined WRS path/row.

## 🚀 Usage

1. Open [Google Earth Engine Code Editor](https://code.earthengine.google.com/)
2. Paste the contents of [`landsat_example`](https://github.com/tomosglaciology/Landsat_Image_Filter/blob/main/Landsat_example) into a new script.
3. Define your area of interest (AOI) by setting a `geometry` variable.
4. Change data filter and WRS path/row to your AOI.

## 🔧 Filtering Options with `funcs`

A summary of the filtering functions available in the `funcs` module, and the associated Landsat data availability:

| Function              | Description                      | Data Availability      |
|-----------------------|----------------------------------|------------------------|
| `funcs.allLandsat`    | Filters **Landsat 4–9**          | 1982 – Present         |
| `funcs.EarlyLandsat`  | Filters **Landsat 4, 5, and 7**  | 1982 – 2025  *(See individual Data Availability for Landsat 4, 5 and 7)*|
| `funcs.NewLandsat`    | Filters **Landsat 8 and 9**      | 2013 – Present  |
| `funcs.Landsat4)`    | Filters only **Landsat 4**       | 1982 – 1993            |
| `funcs.Landsat5`    | Filters only **Landsat 5**       | 1984 – 2013            |
| `funcs.Landsat7`    | Filters only **Landsat 7**       | 1999 – 2025 *(Scan Line Corrector failure after May 2003 )* |
| `funcs.Landsat8`    | Filters only **Landsat 8**       | 2013 – Present         |
| `funcs.Landsat9`    | Filters only **Landsat 9**       | 2021 – Present         |
