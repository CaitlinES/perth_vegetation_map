# Perth Vegetation Map - Multi-Region Setup

This project generates interactive maps for 6 different regions across Perth, displaying tree canopy and vegetation coverage.

## Project Structure

```
docs/
├── index.html          # Home page with buttons linking to each regional map
└── maps/
    ├── perth_inner.html
    ├── perth_north_east.html
    ├── perth_north_west.html
    ├── perth_south_east.html
    ├── perth_south_west.html
    └── mandurah.html
```

## How to Generate Maps

### Option 1: Generate All Regions

Run the R script with all regions:

```r
source("R/Updated_UrbanForest_App.R")
```

This will automatically generate 6 HTML maps in `docs/maps/` folder.

### Option 2: Generate Single Region (Testing)

Edit `R/Updated_UrbanForest_App.R` and uncomment this line:

```r
# For testing, uncomment to generate just one region:
regions_to_generate <- "Perth - South East"
```

Then run:
```r
source("R/Updated_UrbanForest_App.R")
```

## GitHub Pages Setup

The project is configured to use GitHub Pages with the `docs` folder as the source.

1. **Home page** (`docs/index.html`): Displays all 6 region cards with links
2. **Regional maps** (`docs/maps/*.html`): Individual interactive maps

### To Access:

- **Home Page**: `https://YOUR_USERNAME.github.io/perth_vegetation_map/`
- **Regional Maps**: `https://YOUR_USERNAME.github.io/perth_vegetation_map/maps/REGION_NAME.html`

## Available Regions

1. **Mandurah** → `maps/mandurah.html`
2. **Perth - Inner** → `maps/perth_inner.html`
3. **Perth - North East** → `maps/perth_north_east.html`
4. **Perth - North West** → `maps/perth_north_west.html`
5. **Perth - South East** → `maps/perth_south_east.html`
6. **Perth - South West** → `maps/perth_south_west.html`

## Features

- **Interactive Leaflet Maps**: Explore mesh blocks with satellite imagery
- **Detailed Popups**: Click any mesh block to see:
  - Canopy percentage
  - Total vegetation coverage
  - Shrub and grass percentages
  - Walking comfort assessment
  - Ranking relative to Perth
  - Local area (SA2) information

- **Color-Coded Visualization**: Canopy coverage displayed from green (high) to red (low)

- **Home Dashboard**: Beautiful landing page with region cards and statistics

## Data Sources

- **Urban Forest Mesh Blocks 2024**: [DPLH-109 Dataset](https://catalogue.data.wa.gov.au/dataset/urban-forest-mesh-blocks-2024-dplh-109)
- **Map Tiles**: Esri World Imagery
- **Base Geographic Data**: Australian Bureau of Statistics (SA2 boundaries)

## Performance Notes

- Each regional map is a separate HTML file with embedded data
- Maps load faster than a single all-Perth map
- Each map is self-contained and doesn't require external data loads

## File Sizes (Approx)

- Home page: ~15 KB
- Each regional map: 2-5 MB (depending on mesh block count)

## Technologies Used

- **R**: Data processing and map generation
- **Leaflet**: Interactive mapping library
- **htmlwidgets**: R to HTML conversion
- **HTML/CSS**: Home page styling

## Customisation

- [ ] Add comparison mode between regions
- [ ] Add time-series analysis
- [ ] Export map data to GeoJSON
- [ ] Add filtering by vegetation type
- [ ] Create regional statistics dashboard

## License

Data sourced from Western Australia Government. See [DPLH-109 Dataset](https://catalogue.data.wa.gov.au/dataset/urban-forest-mesh-blocks-2024-dplh-109) for data licensing.

---

**App Last Updated**: January 2026
