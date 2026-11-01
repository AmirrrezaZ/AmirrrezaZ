# Hi, I'm Amirreza Zibafar

**Machine learning engineer who takes problems from raw data to a working product.**
I build models for vision, language, tabular and time-series data, and I ship them myself: training, a FastAPI backend, a Postgres database and a React front end.

Aerospace-trained (M.Sc. Flight Dynamics & Control), so I like systems with real constraints: noisy data, limited labels, latency budgets and users who need to trust the numbers.

---

## What I do

| Area | What I've built |
|---|---|
| **Computer vision** | Field boundary segmentation (U-Net / EfficientNet-B7) that beats the FTW and Delineate-Anything baselines. 8× super-resolution with SwinIR. Food-image nutrition estimation. |
| **NLP & multimodal** | Crop disease diagnosis from text (BERT, 90%+ accuracy). A vision-language model for explainable diagnosis that aligns visual symptoms with disease descriptions. |
| **Time series & transformers** | Fine-tuned Presto (a pretrained transformer for satellite time series) for land cover and irrigation. Neural fusion of GraphCast, FuXi and FCN3 for medium-range weather forecasting. |
| **Tabular & decision systems** | Crop recommendation from soil, weather and satellite features. A real-time FX prediction and execution system. Deep models for cancer drug-synergy prediction. |
| **End-to-end engineering** | Python services with FastAPI, PostgreSQL, React front ends, Docker, Linux. Models are packaged as products, not notebooks. |

---

## Selected work

### Models that hold up on data they have never seen
All numbers are measured on held-out data. For land cover the test pixels come from areas the model never saw in training.

| Task | Result |
|---|---|
| **Field boundaries** (Sentinel-2 → 5 m polygons) | Pixel IoU **0.858** vs 0.752 for FTW and 0.677 for Delineate-Anything. PQ **0.223** vs 0.176 and 0.157. The Iran-adapted model retrains only 580 of 67 M parameters on 1,000 tiles. |
| **Irrigation mapping** | Accuracy **0.82**, F1 0.84 (rainfed) / 0.80 (irrigated). Provincial area error 29% against official statistics, versus 134% for an embedding baseline. |
| **Land cover** (11 classes, 10 m) | Accuracy **0.825**, macro-F1 **0.786** on 2.39 M test pixels from unseen regions. |
| **Crop classification** (11 crops) | F1 **0.75** from 24 Sentinel-1/2 observations per season. |
| **Super-resolution** | SwinIR, 8×: Sentinel-2 from 10 m to 1.25 m. |
| **dish2calories** | Re-implemented Nutrition5k with a lighter EfficientNet-B0. Calorie MAE **67.7** vs 70.6, mass MAE **28.6** vs 40.4. |

### From model to product
I worked on the machine learning behind a satellite-analytics platform that answers questions like "what grows here, and is it irrigated?". It covers crops, field boundaries, irrigation, land cover and super-resolution. The model work includes the parts that decide whether people trust a system:

- cloud-robust time series, with radar and interpolation filling cloudy weeks
- spatially separated test sets, so scores describe new places and not memorised ones
- confidence bands on every prediction
- results cached and reused, so the same question is never computed twice

> Part of this work was done at FANAP's Advanced Technologies Lab (ZLab), where I've been an ML engineer since 2022.

---

## Tech stack

**ML:** PyTorch · TensorFlow / Keras · scikit-learn · Hugging Face Transformers · Optuna
**Data:** NumPy · Pandas · SciPy · PostgreSQL · Rasterio · GDAL · GeoPandas
**Backend:** Python · FastAPI · PostgreSQL
**Frontend:** React · Streamlit · Plotly
**Infra:** Docker · Linux · Git · LaTeX
**Also:** MATLAB (control, filtering, optimisation)

---

## Publications

- *Optimization and Design of General Aviation Aircraft Wings Using NSGA-II*, Journal of Aircraft Engineering, 2021. [DOI](https://doi.org/10.22034/joae.2021.303370.1055)
- *Modeling the Ideal Pathway of Plant-Loaded Projectiles for Effective Aerial Reforestation*, 2024.
- *A Review on Airborne Collision Avoidance Systems*, 2022.

---

## Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/amirreza-zibafar-725139199)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:amirzibafar1@gmail.com)
