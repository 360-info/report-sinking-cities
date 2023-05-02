
In order to reproduce the analysis in `analysis/preprocess.qmd`, you will need the [replication data for Tay at al. (2022)](https://researchdata.ntu.edu.sg/dataset.xhtml?persistentId=doi:10.21979/N9/GPVX0F). Place `dataverse_files.zip` in this directory before running the script.

## ♻️ Ready to use

### `data/2-masked`

For each city in the analysis, there are four maps of the subsistence. The maps have been broken up according to how precise the estimates are (as defined by the absolute normalised standard deviation in the velocity):

  - 0 to 25% (most precise)
  - 25 to 50%
  - 50 to 100%
  - morethan 100% (least precise)

If you're looking to create your own map in QGIS, these are probably the most ideal ones for you (you can stack all four up, or make the higher NSD ones semi-transparent).

### `data/3-pngs`

The TIFFs from `data/2-masked` are also available as PNGs for use in the interactive map. They have colour scales set on a per-city basis; refer to `map-bounds-extent.csv` (below) for the `palette_extent`.

I've normalised the standard deviation and then chunked the velocities up into bands of  absolute normalised SD: 0-25%, 25-50%, 50-100%, >100%. 

### `map-bounds-extent.csv`

Statistics for the rasters. Columns include:
 
  - `filename`: name of the raster
  - `ref_lon`, `ref_lat`: lat and lon for each city's "reference point" (velocities are relative to this point)
  - `file_min`, `file_max`: the max and min subsistence for this individual file (not necessarily the whole city), in m/year
  - `palette_extent`: the max absolute velocity across the city. Used to create a colour palette per-city that is symmetrical around zero.
  - `lon_min`, `lon_max`, `lat_min`, `lat_max`: Bounds for the raster in WGS 84 (its native projection)
  - `xmin`, `xmax`, `ymin`, `ymax`: Bounds reprojected to Web Mercator (not needed now).

## ⛔️ Not stored here

A few folders are not version controlled; you must run the analysis script in order to create them:

### `data/src`

The raw, unzipped contents of `dataverse_files.zip`. There are four TIFFs for each city:

  - The observed velocities
  - Interpolated velocities
  - Standard deviations for the observed and interpolated velocities

### `data/1-combined`

Observed and inteprolated velocities and SDs are combined.
