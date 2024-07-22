# Waterline-Jamuna

Supplemental material to: _Combining Earth Observations with Ground Data to Assess River Topography and Morphologic Change: Case Study of the Lower Jamuna River_

Published DDMMYY *to be updated

Journal citation with DOI *to be updated

This repository is distributed under MIT license. The GEE scripts included herein build on other codes previously published by other authors. Please credit me or the previous code authors, as appropriate, for future use of the materials.

# Datasets
Datasets are available through Figshare:
https://doi.org/10.6084/m9.figshare.26339239.v1 

The following subfolders include annual digital elevation model (DEM) datafiles prepared for 2016 to 2019:
- Waterline_DEM_Raw. EM products developed using the waterline method as described in the submitted manuscript (see manuscript Figure 4). The DEMs exclude submerged topography and high-elevation terrain above the high water datum.
- DEM_waterline. Developed by incorporating high-elevation topographic data into the waterline DEM (see manuscript section 3.2)
- DEM_full. Developed by incorporating submerged bathymetry data into the DEM_waterline products (see manuscript section 3.2)

The following subfolders include sloping water mask DEM files for 2017 (see manuscript section 3.1, step 4), as examples for use with the provided GlobalMapper analysis script:
-  WSE_Planes. Sloping water surface planes derived from measured water levels and down-valley linear interpolation
-  WSE_Masks. Sloping water surface masks cropped from the the WSE_Planes data using the extents of detected surface water inundation (see manuscript section 3.1, step 2 and 3).

Metadata for all DEM products are as follows:
- Resolution: 10 m x 10 m
- Vertical datum: Survey of Bangladesh (m, SOB)
- Projection: Transverse Mercator / Gulshan 303 (EPSG:9678)

# Scripts
Extraction of water masks from Sentinel-1 data using GEE in Colab (see manuscript section 3.1, step 2):
[WaterlineJamuna_Sentinel1_WaterDelineation.ipynb](WaterlineJamuna_Sentinel1_WaterDelineation.ipynb)

Extraction of water masks from Sentinel-2 data using GEE in Colab (see manuscript section 3.1, step 2):
[WaterlineJamuna_Sentinel2_WaterDelineation.ipynb](WaterlineJamuna_Sentinel2_WaterDelineation.ipynb)

Processing of water masks into a waterline DEM with GlobalMapper scripting tools (see manuscript section 3.1 and Figure 4, step 5):
[Waterline-Jamuna2017.gms](Waterline-Jamuna-2017.gms)

Processing of water masks into a waterline DEM with GlobalMapper, using a manual version of the script linked above:
[Supplementary GlobalMapper Workflow.pdf](Supplementary GlobalMapper Workflow.pdf)


