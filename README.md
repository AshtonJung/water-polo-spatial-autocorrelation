# High School Water Polo Spatial Autocorrelation Analysis

This repository contains the analysis code used for the manuscript “Geographic Proximity to Strong Competitors and Team Performance in High School Water Polo,” published in the *Journal of Emerging Investigators* ([10.59720/26-046](https://doi.org/10.59720/26-046)).

The study examines whether season-record performance among U.S. high school boys’ water polo teams exhibits spatial clustering. Team performance was measured using reversed end-of-season rankings, and spatial autocorrelation was assessed using global and local Moran’s I analyses.

## Repository contents

* `notebooks/waterpolo_JEI.ipynb`: Main analysis notebook used to process the data, construct spatial weights, compute Moran’s I, and generate figures and tables.
* `data/waterpolo_dataset.csv`: Analytic dataset — 755 teams with location, season record, and strength of schedule.
* `figure/`: Figures included in the manuscript.
* `results/`: Output tables summarizing global and local Moran’s I results.
* `requirements.txt`: Python packages required to run the analysis.

## Data note — de-identification

The published dataset is **school-level only**. The raw file assembled during data
collection also carried staff contact details — athletic director and coach names,
email addresses, direct phone numbers, and street addresses for every school. None
of that was used by the analysis, and it has been removed from this repository and
from its git history.

What remains per team: ranking, school name, city, state, zip, coordinates,
win/loss/draw record, strength of schedule, section, and program level. That is
everything the Moran’s I analysis consumes, so the results below reproduce exactly.

## Key results

Global Moran’s I on k-nearest-neighbour weights (k = 8 primary):

| Sample | n | Moran’s I | Permutation p |
| --- | --- | --- | --- |
| National | 755 | −0.050 | 0.003 |
| California | 571 | −0.040 | 0.014 |

The negative values indicate weak but statistically significant spatial
**dispersion** — neighbouring schools differ more than chance would predict —
rather than the clustering of strong programmes the study set out to test.
Sensitivity across k = 4 to 12 is reported in the notebook; the national estimate
stays negative and significant throughout, while California does not reach
significance at k = 4 or k = 6.
