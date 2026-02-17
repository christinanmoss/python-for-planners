# python-for-planners

# Python for Planners

A ready-to-use Python environment for urban planners covering geospatial analysis, census data, transportation, and more.

## Quickstart

### 1. Install Miniconda (if you don't have it)
Download from: https://docs.conda.io/en/latest/miniconda.html

### 2. Clone this repo
```bash
git clone https://github.com/christinanmoss/python-for-planners.git
cd python-for-planners
```

Or if you don't use Git, click the green **Code** button above → **Download ZIP**, then unzip it.

### 3. Create the environment
```bash
conda env create -f environment.yml
```
This may take 5–15 minutes. Grab a coffee ☕

### 4. Activate it
```bash
conda activate urban-planning
```

### 5. Open in VS Code
```bash
code .
```
Then select the `urban-planning` kernel when prompted (Ctrl+Shift+P → "Python: Select Interpreter").

---

## What's Included

| Category | Libraries | Use Case |
|---|---|---|
| Data wrangling | pandas, numpy, openpyxl | DataFrames, Excel files, math |
| Geospatial core | geopandas, shapely, fiona, pyproj | Shapefiles, GeoJSON, spatial joins |
| Raster/imagery | rasterio, rasterstats, contextily | Satellite imagery, DEMs, basemaps |
| Census & demographics | cenpy, census, pygris | ACS data, TIGER boundaries |
| OpenStreetMap | osmnx, overpy | Street networks, POIs, building footprints |
| Web mapping | folium, ipyleaflet | Interactive maps in Jupyter |
| Spatial statistics | pysal, libpysal, esda, inequality, segregation | Autocorrelation, equity metrics |
| Urban morphology | momepy | Block sizes, street patterns, urban form |
| Visualization | matplotlib, seaborn | Charts, publication-quality figures |
| Notebooks | jupyterlab, ipywidgets | Interactive coding environment |

---

## Census API Key

Some census tools (cenpy, census) require a free API key.  
Get one at: https://api.census.gov/data/key_signup.html

Store it as an environment variable so you're not hardcoding it in notebooks:
```bash
# Mac/Linux — add to your ~/.zshrc or ~/.bashrc
export CENSUS_API_KEY="your_key_here"

# Windows (Anaconda Prompt)
setx CENSUS_API_KEY "your_key_here"
```

Then in Python:
```python
import os
api_key = os.environ.get("CENSUS_API_KEY")
```

---

## Verify Your Setup

Once the environment is active, create a new file and run:

```python
import pandas as pd
import geopandas as gpd
import osmnx as ox
import cenpy
import folium
print("All good, you're ready for class!")
```

If you see the print statement with no errors, you're set!
