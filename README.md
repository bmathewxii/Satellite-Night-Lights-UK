# Satellite  Analysis – UK Night Time Lights as a Proxy for Economic Activity

This project visualises night time light intensity across the UK using VIIRS satellite data from January 2025. Nighttime lights are used as a proxy for economic activity, urbanisation, and infrastructure, with city-level annotations overlaid for visual clarity.

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
```

## Data Preparation

To run this analysis, you'll need to:

1. Download the **VIIRS monthly composite** for desired month from NOAA (radiance-calibrated, `.tgz` format):  
   https://eogdata.mines.edu/download_dnb_composites.html
2. Extract the `.tif` raster file and save it in `data/raw/`
3. Download the UK shapefile (`CTRY_DEC_2024_UK_BGC.shp`) from the ONS Geoportal:  
   https://geoportal.statistics.gov.uk
4. Save all component files in `data/raw/`

## Usage

All processing is done in a single script or Jupyter Notebook. The steps performed are:

1. Clip the VIIRS raster to UK boundaries
2. Apply percentile stretch and gamma correction for contrast enhancement
3. Crop to non-zero light regions to focus on active areas
4. Convert city coordinates to image space for annotation
5. Render final map with dark theme and custom colormap
6. Export PNG and save to output folder

## Results

Output visual has been saved down on the Output folder as part of this repo.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Contact

If you have any questions or feedback, please open an issue in this repository or reach out to me on github.
