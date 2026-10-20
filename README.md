# Automated Marine Habitat Suitability Modelling - Sola Municipality, Norway

## Overview

This project demonstrates a Python-based workflow for automated marine habitat suitability modelling using environmental raster datasets and the Norwegian Nature in Norway (NiN3) marine habitat framework.

The workflow uses bathymetry, slope, wave exposure, light availability, and substrate data to predict the potential distribution of 21 marine habitat types in Sola Municipality, Norway.

All habitat models are generated automatically in Python and combined into a marine habitat richness map to identify areas with high potential biodiversity value.

---

## Study Area

**Sola Municipality, Rogaland, Norway**

The study focuses on the marine and coastal environment of Sola Municipality and demonstrates habitat suitability modelling as a pre-fieldwork decision-support tool for marine habitat assessment.

---

## Project Objectives

- Automate marine habitat suitability modelling using Python
- Apply NiN3-based habitat rules to environmental rasters
- Generate suitability maps for 21 marine habitat types
- Create a combined habitat richness map
- Identify potential biodiversity priority areas
- Develop a reproducible GIS workflow for marine habitat assessment

---

## Input Data

The analysis uses five environmental variables:

### Bathymetry
Water depth raster used to define habitat depth ranges.

### Slope
Seafloor slope derived from bathymetry.

### Wave Exposure
Wave exposure classes representing hydrodynamic conditions.

### Light Availability
Light penetration layer used to identify suitable depth-light relationships.

### Substrate
Seafloor substrate classification used to distinguish habitat preferences.

---

## Workflow

```text
Environmental Variables
(Bathymetry, Slope, Wave, Light, Substrate)
                    │
                    ▼
Raster Alignment
                    │
                    ▼
Suitability Modelling
                    │
                    ▼
21 Marine Habitat Maps
                    │
                    ▼
Habitat Richness Map
                    │
                    ▼
Hotspot Analysis
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

### Geomorphic and Topographic Habitats

- NT-01 Litoralbassengbunn
- NT-04 Litoral bergvegg
- NT-05 Tidevannsmudderflate
- NT-06 Sublitoral grunn sandbunn
- NT-22 Litorale grotter og overheng
- NT-29 Sublitoral bergvegg
- NT-30 Sterke tidevannsstrømmer

---

## Methods

### Data Preparation

All raster datasets were:

- Reprojected to a common coordinate system
- Aligned to a shared raster grid
- Resampled to matching cell size and extent
- Prepared for suitability modelling

### Habitat Suitability Modelling

Each habitat type was represented as a binary suitability model:

```text
1 = Suitable
0 = Unsuitable
```

Suitability criteria were applied using environmental thresholds derived from habitat-specific ecological requirements.

### Habitat Richness Analysis

All habitat layers were combined:

```text
Richness =
NT01 + NT02 + NT03 + ... + NT32
```

The resulting richness raster represents the number of overlapping habitat types per cell.

### Hotspot Analysis

Richness patterns were analysed to identify areas with concentrated habitat diversity and potential priority survey locations.

---

## Results

### Habitat Suitability Maps

- 21 individual habitat suitability layers
- Binary raster outputs for each habitat type

### Habitat Richness Map

The habitat richness analysis identified locations where multiple marine habitat types overlap, highlighting areas of elevated ecological importance.

### Hotspot Map

Hotspot analysis identified clusters of high habitat richness that may represent priority areas for field surveys, habitat verification, and conservation planning.

---

## Technical Implementation

### Python Libraries

- Rasterio
- NumPy
- Matplotlib
- SciPy
- Jupyter Notebook

### GIS Software

- QGIS
- QGIS Model Builder
- Python GIS Automation

---

## Skills Demonstrated

### GIS Skills

- Habitat suitability modelling
- Marine habitat assessment
- Raster processing
- Spatial analysis
- Biodiversity mapping
- Environmental modelling

### Python Skills

- GIS workflow automation
- Raster alignment
- Spatial data processing
- Map generation
- Reproducible analysis
- Batch habitat modelling

### Spatial Analysis Skills

- Multi-criteria suitability analysis
- Habitat richness mapping
- Hotspot analysis
- Environmental variable integration

---

## Key Achievement

Developed an automated Python workflow capable of:

- Loading environmental rasters
- Aligning spatial datasets
- Generating 21 NiN3 habitat suitability maps
- Creating habitat richness maps
- Performing hotspot analysis
- Producing repeatable habitat assessment outputs

This workflow demonstrates how Python can be used to automate marine habitat modelling processes traditionally performed manually within GIS software.

---

## Repository Structure

```text
python_automated_marine_habitat_modelling_sola
│
├── notebooks
