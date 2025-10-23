# How Safe Is NYC?
**Data Bootcamp Midterm Project – Will Wu & John Yue**

This project explores patterns in New York City crime reports using the **NYPD Complaint Data (Historic)** dataset from [NYC Open Data](https://data.cityofnewyork.us/).  
We used Python to perform an end-to-end exploratory data analysis (EDA) that includes data collection, cleaning, feature engineering, visualization, and a simple safety index.

---

## Colab Notebook
View and run the full analysis here:  
[Open in Colab](https://colab.research.google.com/drive/1AOhDGL54ePCcbeNWVK2DcJFgNnrdKVYq?authuser=3)

The notebook mirrors our final report and reproduces every figure used in it.

---

## Project Summary
- **Goal:** Identify which parts of NYC appear safer based on reported police complaints.  
- **Data Source:** NYPD Complaint Data (Historic), dataset ID `qgea-i56i` via Socrata API.  
- **Size:** ~1,000,000 records with mixed numeric, categorical, and spatial data.  
- **Key Skills:** API access, data cleaning, geospatial visualization, and reproducibility.

---

## Method Overview
1. **Setup and Cleaning** – Imported libraries (`pandas`, `seaborn`, `geopandas`, `sodapy`), cleaned inconsistent text, parsed dates, extracted latitude/longitude.
2. **Exploratory Analysis** – Visualized complaint counts by borough, category, and offense type.
3. **Spatial Mapping** – Mapped over one million complaints using GeoPandas and Contextily.
4. **Relative Safety Index (RSI)** – Combined complaint frequency and average severity (Felony = 3, Misdemeanor = 2, Violation = 1) to create a simple comparative metric.
5. **Interpretation** – Discussed borough patterns, emphasizing that complaint volume reflects exposure, not necessarily danger.

---

## Reproducibility
All data are pulled directly from the NYC Open Data API—no manual downloads required.  
To rerun locally:

```bash
pip install pandas numpy matplotlib seaborn geopandas sodapy shapely contextily
