
# Poplar Plantations Classification Uncertainty Analysis

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![GeoPandas](https://img.shields.io/badge/GeoPandas-139C5A?style=flat)
![Rasterio](https://img.shields.io/badge/Rasterio-3776AB?style=flat)
![Dash](https://img.shields.io/badge/Dash-008DE4?style=flat&logo=plotly&logoColor=white)
![LiDAR](https://img.shields.io/badge/LiDAR-2E8B57?style=flat)

Geospatial analysis of poplar plantation classification performance in France using Sentinel-2 confidence rasters and LiDAR metrics.

📍 SIGMA Master – UE1002 “Atelier Géomatique”
Agro Toulouse (ENSAT) · Université Toulouse II – Jean Jaurès


---

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

<p align="center">
  <img src="rapport/diagramme/diagramme_traitement.png" alt="Workflow diagram" width="500">
</p>

---

### 📈 **Key Analyses**

* Temporal evolution of classification confidence by plantation age
* Cultivar-specific uncertainty analysis
* Correlation between LiDAR metrics and classification performance
* Identification of minimum plantation age for reliable classification (~5 years)

All box-notch visualizations are available in the [`/results`](./results) folder:

* [Overall confidence vs age](./results/1_confidenceXage/Boxnotch_confidenceXage_all.pdf)
* [Top cultivars confidence vs age](./results/1_confidenceXage/Boxnotch_confidenceXage_top_cultivars.pdf)
* [Per year analysis](./results/2_confidenceXage_par_annee/Boxnotch_confidenceXage_par_annee.pdf)
* [LiDAR metrics vs age](./results/3_lidar_metrics/Boxnotch_lidar_metrics_top_cultivars.pdf)
* [Confidence & LiDAR combined](./results/4_confidenceXage_lidar_metrics/Boxnotch_confidenceXage_lidar_metrics_top_cultivars.pdf)

---

### 🖥️ **Interactive Visualization**

Two interactive Dash applications were developed:

* `7_0_App_un_graphique.py` — single interactive plot explorer
* `7_1_App_px_confidenceXage.py` — dual-plot comparison mode

They allow cultivar selection, variable choice (X/Y), hover inspection and faceted temporal views.

---

### 📂 **Repository Structure**

```
UE1002_Peupleraie/
├── data_brut/                # Raw raster & vector datasets
├── data_final/               # Preprocessed aligned data
├── scripts/                  # Jupyter notebooks + Python functions
├── results/                  # Boxnotch figures & analyses
├── rapport/                  # Project report & diagrams
└── README.md
```

---

### 🧠 **Key Skills & Tools**

* 🛰 Sentinel-2 time series analysis
* 🌳 LiDAR metrics integration (Canopy Cover, PAI)
* 🐍 Python geospatial stack (GeoPandas, Rasterio, Plotly/Dash)
* 📊 Box-notch visualization for statistical uncertainty analysis
* 🗂 GIS data preparation, masking & spatial joins

---

### 📚 **Reference**

Based on the project report:

> *Abir Ben Abdelghaffar, Lucas Lima, Naly Rakotoarindrazaka (2023). UE1002 – Analyse de l’incertitude de classification de peupleraies plantées.*

---
