# High School Water Polo Spatial Autocorrelation Analysis

This repository contains the analysis code used for the manuscript “Geographic Proximity to Strong Competitors and Team Performance in High School Water Polo.”

The study examines whether season-record performance among U.S. high school boys’ water polo teams exhibits spatial clustering. Team performance was measured using reversed end-of-season rankings, and spatial autocorrelation was assessed using global and local Moran’s I analyses.

## Repository contents

* `notebooks/waterpolo_spatial_analysis.ipynb`: Main analysis notebook used to process the data, construct spatial weights, compute Moran’s I, and generate figures and tables.
* `data/waterpolo_final_2024_2025.csv`: Final analytic dataset used in the study.
* `figures/`: Figures included in the manuscript.
* `results/`: Output tables summarizing global and local Moran’s I results.
* `requirements.txt`: Python packages required to run the analysis.

## Data

The dataset represents U.S. high school boys’ water polo teams from the 2024–2025 season and was finalized on January 23, 2025. The data were compiled from publicly available team ranking and school location sources. No individual-level student data or personally identifiable information are included.

## Reproducibility

To reproduce the analysis, install the required packages and run the notebook from top to bottom.

## Software

The analysis was conducted in Python using open-source libraries including pandas, GeoPandas, PySAL/libpysal, esda, NumPy, and matplotlib.
