# Automated Marine Habitat Suitability Modelling and Hotspot Analysis - Sola Municipality, Norway

## Overview

This project demonstrates an end-to-end Python GIS workflow for automated marine habitat suitability modelling, habitat richness assessment, and hotspot analysis.

Using environmental raster datasets and habitat-specific suitability criteria, 21 marine NiN3 habitat types were modelled for Sola Municipality, Norway. Individual suitability layers were combined to generate a habitat richness map and a Getis-Ord Gi* hotspot analysis was performed to identify clusters of habitat-rich areas.

The project showcases how Python can automate GIS workflows traditionally performed manually in desktop GIS software.

---

## Study Area

**Sola Municipality, Rogaland, Norway**

The study focuses on the marine and coastal environment of Sola Municipality and demonstrates how spatial modelling can support marine habitat assessment and biodiversity prioritization.

---

## Project Objectives

- Automate marine habitat suitability modelling using Python
- Apply NiN3-based habitat suitability rules
- Generate suitability maps for 21 marine habitat types
- Create a marine habitat richness map
- Perform Getis-Ord Gi* hotspot analysis
- Identify potential biodiversity priority areas
- Develop a reproducible GIS workflow

---

## Input Environmental Variables

The analysis utilizes five environmental raster datasets:

### Bathymetry
Depth information used to define habitat-specific depth ranges.

### Slope
Seafloor slope derived from bathymetric data.

### Wave Exposure
Hydrodynamic exposure classes representing wave conditions.

### Light Availability
Environmental suitability based on underwater light penetration.

### Substrate
Seafloor substrate classification used to define habitat preferences.

---

## GIS Workflow

```text
Environmental Variables
(Bathymetry, Slope, Wave, Light, Substrate)
                    │
                    ▼
Raster Alignment
                    │
                    ▼
21 Habitat Suitability Models
                    │
                    ▼
Habitat Richness Map
                    │
                    ▼
Raster-to-Point Conversion
                    │
                    ▼
GeoPandas & PySAL
                    │
                    ▼
Getis-Ord Gi* Hotspot Analysis
                    │
                    ▼
Priority Marine Areas
```

---

## Habitat Types Modelled

### Marine Macroalgae and Kelp Habitats

- NT-03 Tangsamfunn
- NT-14 Sukkertareskog
- NT-16 Stortareskog
- NT-18 Fingertareskog
- NT-20 Butareskog
- NT-21 Ruglbunn

### Seagrass and Coastal Vegetation

- NT-09 Marin tidevannssump
- NT-10 Ålegrasbunn
- NT-11 Dvergålegrasbunn
- NT-13 Brakkvanns-undervannseng
- NT-32 Pusleplantebunn

### Shell Habitats

- NT-02 Blåskjellbunn
- NT-07 Flatøstersbunn
- NT-08 O-skjellbunn

### Topographic and Geomorphic Habitats

- NT-01 Litoralbassengbunn
- NT-04 Litoral bergvegg
- NT-05 Tidevannsmudderflate
- NT-06 Sublitoral grunn sandbunn
- NT-22 Litorale grotter og overheng
- NT-29 Sublitoral bergvegg
- NT-30 Sterke tidevannsstrømmer

---

## Methodology

### 1. Data Preparation

Environmental raster datasets were:

- Loaded in Python
- Checked for spatial consistency
- Aligned to a common grid
- Resampled to matching extent and resolution

### 2. Habitat Suitability Modelling

Each habitat type was modelled using habitat-specific environmental thresholds.

Suitability outputs were generated as binary rasters:

```text
1 = Suitable Habitat
0 = Unsuitable Habitat
```

### 3. Habitat Richness Analysis

All habitat models were combined into a single richness raster:

```text
Richness =
NT01 + NT02 + NT03 + ... + NT32
```

The resulting richness map represents the number of habitat types occurring at each location.

### 4. Hotspot Analysis

Habitat richness values were converted to points and analysed using:

- GeoPandas
- PySAL
- Getis-Ord Gi*

The analysis identifies spatial clusters of habitat-rich areas and highlights potential biodiversity hotspots.

---

## Results

### Habitat Suitability Maps

Generated:

- 21 individual marine habitat suitability layers
- Binary habitat presence/absence maps
  
### Habitat Richness Map

The combined richness raster reveals areas where multiple habitat types overlap and where ecological diversity is potentially highest.

<img width="2083" height="1997" alt="richness_map" src="https://github.com/user-attachments/assets/84b689a9-51bf-4e48-8d9e-ec291ff9f3d6" />


### Getis-Ord Gi* Hotspot Analysis

Hotspot analysis identified spatial patterns in habitat richness and highlighted areas exhibiting elevated clustering of habitat diversity.

<img width="2467" height="2433" alt="hotspot_map" src="https://github.com/user-attachments/assets/04878160-c4ec-49f8-ba71-896776c7a33a" />


---

## Technologies Used

### GIS Software

- QGIS
- QGIS Model Builder

### Python Libraries

- Rasterio
- NumPy
- GeoPandas
- PySAL
- SciPy
- Matplotlib
- Pandas
- Jupyter Notebook

---

## Skills Demonstrated

### GIS Analysis

- Habitat Suitability Modelling
- Raster Processing
- Spatial Analysis
- Biodiversity Mapping
- Environmental Modelling
- Marine GIS

### Python GIS

- Rasterio
- GeoPandas
- PySAL
- NumPy
- Spatial Statistics
- Jupyter Notebook Workflows

### GIS Automation

- Automated Raster Alignment
- Automated Habitat Modelling
- Batch GIS Processing
- Habitat Richness Mapping
- Automated Spatial Analysis

### Spatial Statistics

- Getis-Ord Gi* Hotspot Analysis
- Spatial Weights Construction
- Point-Based Spatial Analysis
- Cluster Detection

---

## Key Achievement

Developed a fully automated Python workflow capable of:

- Loading environmental raster datasets
- Aligning spatial layers
- Generating 21 marine habitat suitability models
- Creating habitat richness maps
- Performing Getis-Ord Gi* hotspot analysis
- Exporting GIS-ready outputs

This project demonstrates the integration of raster GIS, vector GIS, spatial statistics, and automation within a reproducible Python workflow.

---

## Repository Structure

```text
sola-marine-habitat-modelling
│
├── notebooks/
│   └── Automated_Habitat_Suitability_Sola.ipynb
│
├── figures/
│   ├── richness_map.png
│   ├── hotspot_map.png
│   └── nt14_example.png
│
├── outputs/
│   ├── richness.tif
│   ├── hotspot_points.gpkg
│   └── habitat_rasters/
│
├── docs/
│   └── Sola_Expression.xlsx
│
└── README.md
```

---

## Data Availability

Original environmental raster datasets are not included in this repository due to file size and data ownership considerations.

The workflow can be reproduced using equivalent raster datasets representing:

- Bathymetry
- Slope
- Wave Exposure
- Light Availability
- Substrate

---

## Future Improvements

Potential future developments include:

- One-click habitat modelling tools
- Automated reporting
- Interactive web mapping
- Regional-scale habitat modelling
- Species observation integration
- Machine learning habitat prediction

---

## Author

**Arjuman Banu**

GIS | Marine Habitat Modelling | Spatial Analysis | Python GIS Automation

This project demonstrates the application of Python-based GIS automation for marine habitat suitability modelling, habitat richness mapping, and spatial hotspot analysis.
