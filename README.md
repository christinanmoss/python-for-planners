# python-for-planners

# Planning Python Environment

A ready-to-use Python environment for city planners covering geospatial analysis, census data, transportation, and more.

## Quickstart

### 1. Install Miniconda (if you don't have it)
Download from: https://docs.conda.io/en/latest/miniconda.html

### 2. Clone this repo
```bash
git clone https://github.com/YOUR_USERNAME/planning-python-env.git
cd planning-python-env
```

### 3. Create the environment
```bash
conda env create -f environment.yml
```

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

| Category | Libraries |
|---|---|
| Data wrangling | pandas, numpy, openpyxl |
| Geospatial core | geopandas, shapely, fiona, pyproj |
| Raster/imagery | rasterio, rasterstats, contextily |
| Census & demographics | cenpy, census, pygris |
| OpenStreetMap | osmnx, overpy |
| Web mapping | folium, ipyleaflet |
| Spatial statistics | pysal, libpysal, esda, inequality, segregation |
| Urban morphology | momepy |
| Visualization | matplotlib, seaborn |
| Notebooks | jupyterlab, ipywidgets |

---

## Census API Key

Some census tools (cenpy, census) require a free API key.  
Get one at: https://api.census.gov/data/key_signup.html

Store it as an environment variable so you're not hardcoding it in notebooks:
```bash
# Mac/Linux — add to your ~/.zshrc or ~/.bashrc
export CENSUS_API_KEY="your_key_here"

# Windows (Command Prompt)
setx CENSUS_API_KEY "your_key_here"
```

Then in Python:
```python
import os
api_key = os.environ.get("CENSUS_API_KEY")
```
