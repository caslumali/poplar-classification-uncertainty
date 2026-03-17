# Poplar Plantations Classification Uncertainty Analysis

<<<<<<< HEAD
Classification uncertainty analysis combining Sentinel-2 confidence rasters, LiDAR metrics, and statistical visualization for poplar plantations in France.
=======
# Poplar Plantations Classification Uncertainty Analysis

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![GeoPandas](https://img.shields.io/badge/GeoPandas-139C5A?style=flat)
![Rasterio](https://img.shields.io/badge/Rasterio-3776AB?style=flat)
![Dash](https://img.shields.io/badge/Dash-008DE4?style=flat&logo=plotly&logoColor=white)
![LiDAR](https://img.shields.io/badge/LiDAR-2E8B57?style=flat)

Geospatial analysis of poplar plantation classification performance in France using Sentinel-2 confidence rasters and LiDAR metrics.

📍 SIGMA Master – UE1002 “Atelier Géomatique”
Agro Toulouse (ENSAT) · Université Toulouse II – Jean Jaurès
>>>>>>> f1951e30b033d7f437b35005350d1edf0cba441c

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![GeoPandas](https://img.shields.io/badge/GeoPandas-139C5A?style=flat)
![Rasterio](https://img.shields.io/badge/Rasterio-3776AB?style=flat)
![Dash](https://img.shields.io/badge/Dash-008DE4?style=flat&logo=plotly&logoColor=white)
![LiDAR](https://img.shields.io/badge/LiDAR-2E8B57?style=flat)

---

<<<<<<< HEAD
## Overview

This repository contains a geospatial workflow for analysing the uncertainty of poplar plantation classification in France.

The project combines:

- Sentinel-2 confidence rasters from 2017 to 2022
- LiDAR structural metrics such as canopy cover and PAI
- vector parcel data with plantation age and cultivar information
- statistical visualization and interactive exploration

The main objective was to understand how classification confidence varies with plantation age, cultivar type, and structural characteristics derived from LiDAR.

---

## Study area and data

The analysis covers four French departments across five Sentinel-2 tiles.

Main data sources:

- Sentinel-2 confidence rasters based on the PI spectral index
- IGN LiDAR metrics at 10 m resolution
- parcel-level vector data with cultivar, planting date, and derived attributes

---

## Workflow

The pipeline was developed in Python using notebooks and geospatial libraries for raster and vector processing.

Main steps:

1. Clean and prepare vector parcel data.
2. Reproject, clip, and align raster datasets.
3. Extract raster values and join them to plantation polygons and pixel samples.
4. Filter inconsistent observations and derive analysis tables.
5. Produce statistical visualizations and interactive dashboards.
=======
## 🌍 **Project Overview**

This module focused on analysing the classification uncertainty of poplar plantations (*peupleraies*) across French territories, using:

- Time series of confidence rasters (2017–2022) produced with the PI spectral index;
- High-resolution LiDAR structural metrics (Canopy Cover and PAI);
- Vector data of agricultural parcels containing age and cultivar information for each plantation.

The main objective was to evaluate how classification probability varies as a function of:

- plantation age;
- cultivar type;
- LiDAR metrics representing structural characteristics.

---

## 🧭 **Study Area & Data**

- 4 French departments (47, 82, 73, 10) covering 5 Sentinel-2 tiles.
- Sentinel-2 data (2017–2022), confidence rasters (PI Index).
- IGN LiDAR metrics (2021–2023) at 10 m resolution (CC, PAI).
- Vector data containing cultivars, planting dates, and derived attributes.

---

## 🧪 **Methodological Workflow**

The pipeline was entirely developed in Python 3.10, using Jupyter Notebooks and geospatial libraries (GeoPandas, Rasterio, Dash, Plotly).

Workflow in 5 steps:

1. Cleaning & preparation of vector data (`1_Nettoyage_gpkg.ipynb`)
2. Stacking, reprojection & clipping of raster datasets (`2_Masquage_rasters.ipynb`)
3. Raster value extraction & spatial join with vector data (`3_Extraction_valeurs.ipynb`)
4. Filtering & consistency checks (dates, canopy thresholds) (`4_Filtrage_csv.ipynb`)
5. Statistical visualization using box-notch plots and interactive Dash apps
>>>>>>> f1951e30b033d7f437b35005350d1edf0cba441c

<p align="center">
  <img src="rapport/diagramme/Chaine_Traitement_2025-01-15.png" alt="Workflow diagram" width="520">
</p>

---

## Key analyses

The repository documents several complementary analyses:

- temporal evolution of classification confidence by plantation age
- cultivar-specific patterns of uncertainty
- relationships between classification confidence and LiDAR metrics
- combined age, confidence, and structure analysis
- identification of the age threshold at which classification becomes more reliable

Selected outputs are available in the [`results/`](./results) folder, including:

- overall confidence versus age
- yearly confidence-versus-age comparisons
- LiDAR metrics versus age
- combined confidence and LiDAR visualizations

---

## Interactive tools

The project also includes Dash applications for interactive exploration:

- `7_0_App_un_graphique.py` for single-plot exploration
- `7_1_App_px_confidenceXage.py` for comparing confidence and age relationships
- `7_2_App_px_metriques_lidar.py` for exploring LiDAR-related indicators

These apps support cultivar selection, variable comparison, and interactive inspection of temporal and structural patterns.

---

## Repository structure

```text
1002-703_Projet/
|-- data_brut/      # Raw raster and vector data
|-- data_final/     # Processed raster, vector, and tabular outputs
|-- scripts/        # Notebooks, Python functions, and Dash apps
|-- results/        # Statistical figures and exported analyses
|-- rapport/        # Report material and workflow diagrams
`-- README.md
```

---

## Why this repository matters

This repository shows:

- uncertainty analysis for remote-sensing classification outputs
- integration of Sentinel-2 and LiDAR information
- geospatial data preparation with Python
- parcel- and pixel-level statistical analysis
- interactive visualization of classification behaviour

---

## Context

This project was developed during the SIGMA MSc in France as part of the UE1002 geospatial workshop. It remains a strong example of applied geospatial analysis combining Earth observation, LiDAR, and statistical interpretation.
