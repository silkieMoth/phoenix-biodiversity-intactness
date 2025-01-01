# The Biodiverisity Intactness Index and Biodiveristy Decline in Phoenix, AZ

## About
This repository is part of an assignment for the class EDS-220 Environmental Datasets at University of California, Santa Barbara as part of the Master's of Environmental Data Science program with the Bren School for Environmental Science and Management. 

It contains code for analysis of biodiversity decline in the Phoenix-Mesa-Chandler Metropolitan Statistical District. By sourcing data for a Biodiversity Intactness Index (BII), we quantify change in an area's biodiversity on a temporal scale. 

![Chollas and Saguaros](/images/sonoran-desert.jpg "Sonoran landscape with Chollas and Saguaros.")

## Repository Structure
### Files
* `final_proj_part_2.ipynb` contains all code for...
    + Subsetting the US Census Bureau TIGER shapefile for Phoenix.
    + Interfacing with Planetary Computer STAC Collection for the `io-biodiversity` dataset.
    + Clipping the `io-biodiversity` raster's to the Phoenix polygon.
    + Calculating total area where BII is greater than 0.75.
    + Creating masked raster for biodiversity loss from 2017 to 2020, where areas that formerly had a BII >= 0.75 have declined below that standard.
    + Plotting...
        - The broader geographic context of the Phoenix-Mesa-Chandler MSD.
        - BII index raster with locations of decline from >= 0.75 to < 0.75.


### File Organization

```
BII-biodiversity-decline
│
├── README.md                     
├── final_proj_part_2.ipynb  # .ipynb for conducting biodiversity analysis
│
├── images/                       
│   ├── sonoran-desert.jpg             # image used in the README
│
├── .gitignore 
```

## Data 
The data needed for this analysis is not stored in the repository. The datasets can be loaded from their own respective sources.

* `io-biodiversity` can be accessed by interfacing with Microsoft's Planetary Computer STAC Collection API directly in python, utilizing the `pystac_client` and `planetary_computer` libraries. The code and instructions for which to accomplish this is included in the "final_proj_part_2" notebook.
* `tl_2021_04_cousub.shp` (US Census Bureau & Department of Commerce's 2021 TIGER/Line Shapefile for county subdivisions in AZ) can be downloaded from [Data.gov](https://catalog.data.gov/dataset/tiger-line-shapefile-2021-state-arizona-county-subdivisions). Code and instructions to subset for the Phoenix polygon are included in the "final_proj_part_2" notebook.

## References
### Acknowledgements
#### This project is supported in part by:
- EDS 220 Environmental Datasets at UCSB: [Website](https://meds-eds-220.github.io/MEDS-eds-220-course/)
- UCSB Bren School for Environmental Science and Management: [Website](https://bren.ucsb.edu/)
- The Master of Environmental Data Science degree at Bren: [Website](https://bren.ucsb.edu/masters-programs/master-environmental-data-science)
- National Center for Ecological Analysis and Synthesis (NCEAS): [Website](https://www.nceas.ucsb.edu/)
- Sam Csik: [Website](https://samanthacsik.github.io/)

### Data Citations
Impact Observatory, Vizzuality (2022). *io-biodiversity* (v1) [Dataset]. Microsoft Planetary Computer STAC Catalog. https://planetarycomputer.microsoft.com/dataset/io-biodiversity#overview

Department of Commerce. (2021). *TIGER/Line Shapefile, 2021, State, Arizona, County Subdivisions* [Dataset]. U.S. Census Bureau. https://catalog.data.gov/dataset/tiger-line-shapefile-2021-state-arizona-county-subdivisions
