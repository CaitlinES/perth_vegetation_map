# Quick Start Guide - Multi-Region Maps

## What Changed

Your project now generates **6 separate regional maps** plus a **home dashboard**.

## File Structure

```
docs/
├── index.html                    ← HOME PAGE (new!)
└── maps/
    ├── mandurah.html            ← GENERATED MAPS (new folder!)
    ├── perth_inner.html
    ├── perth_north_east.html
    ├── perth_north_west.html
    ├── perth_south_east.html
    └── perth_south_west.html
```

## Step 1: Generate All Maps

Run this in R:
```r
setwd("d:/Fun_Scripts/perth_vegetation_map")
source("R/Updated_UrbanForest_App.R")
```

This will generate all 6 regional maps in `docs/maps/` folder.

**First run may take 10-20 minutes** (depending on your computer).

## Step 2: Push to GitHub

```powershell
cd "d:\Fun_Scripts\perth_vegetation_map"
git add .
git commit -m "Generate all regional maps"
git push origin main
```

## Step 3: View on GitHub Pages

Your site will be live at:
- **Home**: `https://CaitlinES.github.io/perth_vegetation_map/`
- **Maps**: `https://CaitlinES.github.io/perth_vegetation_map/maps/REGION.html`

(Replace `CaitlinES` with your GitHub username)

## Customizing the Home Page

Edit `docs/index.html` to change:

1. **Colors** (around line 75):
   ```css
   .inner { background: linear-gradient(135deg, #c41c3b 0%, #e74c3c 100%); }
   ```

2. **Descriptions** (around line 172):
   ```html
   <p class="map-description">Your custom text here</p>
   ```

3. **Icons** (around line 164):
   ```html
   <div class="map-card-icon">🏙️</div>
   ```

## Testing Single Region

To test with just one region (faster), edit `R/Updated_UrbanForest_App.R` line 45:

```r
# Uncomment this line:
regions_to_generate <- "Perth - South East"

# Comment out (add # before) the full list above
```

Then run just that region's map generation.

## Website Preview

Your home page will show:
- 6 colorful cards (one per region)
- "View Map" button on each card
- Information about the project
- Links to data sources

Each card links to its regional map where visitors can:
- Click any mesh block to see details
- Zoom in/out
- Toggle between satellite and other base maps
- See rankings and statistics

## Important Notes

⚠️ **File Sizes**: Each regional map is 2-5 MB (self-contained HTML with embedded map data)

✅ **GitHub Pages Limit**: Free accounts can host up to 1 GB, so you have room for these maps

📱 **Mobile Friendly**: Home page and maps are fully responsive

🔗 **Links**: The home page at `index.html` automatically links to `maps/region.html` files

## Next Steps

1. ✅ Run the R script to generate all maps
2. ✅ Commit and push to GitHub
3. ✅ Wait 1-2 minutes for GitHub Pages to build
4. ✅ Share your site link with anyone!

---

**Questions?** Check `SETUP_GUIDE.md` for more detailed information.
