# Geo Data Inspector

A lightweight collection of Python/Jupyter workflows for **inspecting geospatial and tabular datasets before saving or processing them locally**.

The first notebook focuses on online CSV files. The repository is intentionally structured so it can later grow to cover Shapefiles, GeoPackages and Esri geodatabases.

## Current workflow: online CSV preview

The notebook reads a CSV directly from a URL into a pandas DataFrame, allowing you to:

- inspect the dataset without first downloading it manually;
- view its row/column structure, field names and data types with `DataFrame.info()`;
- preview the first 10 records;
- decide whether the dataset is useful; and
- save it locally only when `save_csv = True`.

## Usage

1. Open `geo_data_inspector.ipynb` in Jupyter Notebook or JupyterLab.
2. Add the source CSV URL:

```python
url = "https://example.com/data.csv"
```

3. Run the notebook and inspect the output.
4. By default the notebook does not save the dataset:

```python
save_csv = False
```

5. If the dataset looks useful, set the output path and change the flag:

```python
output_path = r"C:\data\my_data.csv"
save_csv = True
```

6. Rerun the final cell to save the DataFrame as a CSV.

## Requirements

- Python 3
- pandas
- Jupyter Notebook or JupyterLab

Install the main dependency with:

```bash
pip install pandas
```

## Planned extensions

Future notebooks or modules can extend the same **inspect first, save/use later** approach to:

- Shapefile (`.shp`)
- GeoPackage (`.gpkg`)
- Esri file geodatabase (`.gdb`)
- potentially GeoJSON and other common spatial formats

For spatial formats, GeoPandas and/or GDAL-based libraries would be natural options to evaluate as the repository expands.

## Repository structure

```text
geo-data-inspector/
├── README.md
└── inspect_online_csv.ipynb
```

## Repository name

**Recommended:** `geo-data-inspector`

This is broader than `csv-inspector`, so it still fits when spatial formats are added later.
