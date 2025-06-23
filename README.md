# MODIS NDVI & LST Long-Term Monitoring over Rubber Plantation Field (2000–2025)

![image](https://github.com/user-attachments/assets/eb15e5fc-96f6-4ba9-80b1-33750bcb1a60)


## 📍 Background

Rubber plantations are critical agroecosystems in Southeast Asia, and monitoring their long-term vegetation health and surface temperature trends is essential for understanding climate impacts and land surface processes.

This project focuses on a rubber plantation field in **Songkhla, Thailand**, using **Google Earth Engine (GEE)** to analyze over 20 years of satellite data.

---

## 🎯 Objective

To extract, visualize, and export long-term time series of:

* **NDVI** (Normalized Difference Vegetation Index)
* **LST** (Land Surface Temperature in °C)

...using **MODIS MOD13Q1 (NDVI)** and **MODIS MOD11A2 (LST)** collections over a defined plantation polygon.

---

## 🧰 Materials

* Rubber plantation boundary polygon (GEE Asset): `projects/ee-my-konlavach/assets/RubberPlantation`
* MODIS MOD13Q1 NDVI (16-day, 250m resolution)
* MODIS MOD11A2 LST Daytime (8-day, 1km resolution)
* Google Earth Engine JavaScript API

---

## 🧪 Methods

1. Filter MODIS NDVI and LST collections by date and AOI
2. Clip and scale each image to get NDVI and LST in real units
3. Calculate mean NDVI and LST for each image over the AOI
4. Merge the statistics by date
5. Export:

   * Time series charts
   * Monthly/yearly trends
   * CSV tables
   * Animated seasonal GIFs

---

## 📊 Results

### NDVI and LST Time Series

* ![image](https://github.com/user-attachments/assets/8da9d4a7-dee6-4e77-abdb-04990b4e4cf1)
* ![image](https://github.com/user-attachments/assets/0a4a33d3-4a7d-4d93-a5a5-2b6d5d3cb8d9)

![image](https://github.com/user-attachments/assets/739a29eb-4938-47ce-820c-84a4de0767b7)

### Animated GIFs

* 
* 

### Monthly/Yearly Trends (Printed to Console)

* Monthly NDVI average (Jan–Dec)
* Yearly LST average (2000–2025)

### Exported Files

* `NDVI_monthly_stats.csv`
* `LST_monthly_stats.csv`
* `NDVI_LST_merged.csv`
* `NDVI_animation.mp4`
* `LST_animation.mp4`

---

## 📂 Repository Contents

```text
📁 figures/
   ├── ndvi_animation.gif
   ├── lst_animation.gif
   └── ndvi_lst_chart.png
📁 exports/
   ├── NDVI_monthly_stats.csv
   ├── LST_monthly_stats.csv
   └── NDVI_LST_merged.csv
📄 modis_ndvi_lst_analysis.js
📄 README.md
```

---

## 🛠️ How to Use

1. Upload your polygon to your GEE assets
2. Load and run the script in [Google Earth Engine Code Editor](https://code.earthengine.google.com/)
3. Adjust time range, scale, or AOI if needed
4. Run exports and download from GEE Tasks tab

---

## 📌 Notes

* LST values are converted to °C
* NDVI is scaled by 0.0001 (MODIS standard)
* The script uses `.reduceRegion()` for statistical summaries

---

## 🔄 Next Steps

* Compare MODIS vs Sentinel-2 trends
* Add phenological metrics (NDVI max, SOS/EOS)
* Rainfall correlations (optional)

---

Code: https://code.earthengine.google.com/1e96ca4201a19979fe16912fa17bd850

© 2025 Konlavach Mengsuwan · ZALF · Google Earth Engine
