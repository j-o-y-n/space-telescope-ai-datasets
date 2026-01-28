# Space Telescope AI Dataset

This repository contains **processed, light curve datasets** derived from NASA’s Kepler, K2, and TESS missions.  
These files are used by the Space Telescope Kids AI web application.

---

## 📁 Contents

- `planets/` — processed light curves containing real exoplanet transits  
- `non_planets/` — stars with no known planets  
- `false_positives/` — variable stars, binaries, or noise patterns  
- `index.json` — dataset index used by the web app

---

## 🛰️ Data Sources

This project uses publicly available data produced by NASA’s **Kepler**, **K2**, and **TESS** missions.

Original data was accessed through the **Mikulski Archive for Space Telescopes (MAST)**  
and processed using the **Lightkurve** Python library.

- NASA data is **public domain** (U.S. Government work)  
- Lightkurve documentation: https://lightkurve.github.io/

---

## 🔧 Processing Steps

All light curves in this repository were processed using the following pipeline:

1. Download using Lightkurve  
2. Remove NaNs and outliers  
3. Detrend using Savitzky–Golay flattening  
4. Normalize flux  
5. Downsample to fixed length (e.g., 384 points)  
6. Export to compact JSON format

---

## 📜 License

Original NASA data is **public domain**.

All processed datasets in this repository  
(cleaned, normalized, resampled JSON files and labels)  
are released under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**.

Full license text:  
https://creativecommons.org/licenses/by/4.0/

---

## 🙌 Attribution

If you use this dataset, please cite:

- NASA Kepler / K2 / TESS missions  
- MAST archive  
- Lightkurve Python package  
- This repository
