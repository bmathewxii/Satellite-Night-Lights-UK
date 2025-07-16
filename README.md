# Satellite  Analysis – UK Night Time Lights as a Procy for Economic Growth

This project visualises night time light intensity across the UK using VIIRS satellite data from January 2025. Nighttime lights are used as a proxy for economic activity, urbanisation, and infrastructure, with city-level annotations overlaid for visual clarity.

The final result is a heatmap of the UK.

## Data Sources

- **UK Country Boundaries (ONS)**: https://geoportal.statistics.gov.uk
- **VIIRS Nighttime Lights (NOAA)**: https://eogdata.mines.edu/download_dnb_composites.html

## Annotated Cities

The map includes the following major cities for ease of visualisation:

- London
- Birmingham
- Manchester
- Leeds
- Glasgow
- Edinburgh
- Belfast
- Cardiff
- Bristol
- Newcastle

## Requirements

- Python 3.8+
- Dependencies:
  - geopandas
  - rasterio
  - numpy
  - matplotlib

Install dependencies via:

```bash
pip install geopandas rasterio numpy matplotlib
