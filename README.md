# 🥕 Predictive Modeling for Carrot Quality, Carotenoid Content, and Damage Classification  
### Article — Spectral Techniques, Colorimetry & Artificial Intelligence

This repository contains the code used in the **article on predictive modeling of carotenoid content and damage classification in carrots using spectral techniques, colorimetry, and artificial intelligence**, developed within the SGR-funded project:

**“Strengthening the Carrot Production Chain” (BPIN 2020000100192).**

The raw datasets used to run all models presented in the article are available at the DOI:

🔗 https://doi.org/10.5281/zenodo.17872167

---

## 📡 Overview of Models and Analytical Pipelines

This repository integrates multiple **machine-learning**, **spectral**, and **imaging** workflows for carrot quality assessment under field and laboratory conditions.

---

## 🌱 1. Phenology Classification Model (UAV Orthomosaics)

A machine-learning model trained on **spectral indices extracted from drone-based multispectral orthomosaics** to classify carrot crop phenological stages.

---

## 🌈 2. Carotenoid Regression Model From Orthomosaics  

A regression model for **estimating carotenoid content** directly from spectral vegetation indices obtained from UAV orthomosaics, enabling **non-destructive biochemical approximation** under field conditions.

---

## 🔬 3. High-Resolution Carotenoid Model From Laboratory Spectroradiometer Signatures

A regression model built using **VIS–NIR spectral signatures (350–2500 nm)** acquired in controlled laboratory conditions using a **Spectral Evolution spectroradiometer**.

This model enables **high-fidelity carotenoid prediction** from precise reflectance measurements.

---

## 🎨 4. RGB-Based Carotenoid Estimation Using a Custom Color Index (ICarot)

Workflow includes:

- Extraction of **CIELAB color features (L*, a*, b*)**
- Calculation of a custom pigment-sensitive index **ICarot**
- Calibration against laboratory carotenoid measurements
- Classification into **Low, Medium, High** carotenoid levels

Formula used for the index:

<img width="520" height="67" alt="image" src="https://github.com/user-attachments/assets/99e6b2f1-51c3-411f-9507-3da25044cb4d" />
b*=Yellow-blue axis, associated with carotenoid content (e.g., β-carotene).
a* = Red-green axis, representing the contribution of secondary pigments.
C = Color saturation, related to pigment purity.
b*max,a*max, cmax= Maximum values for each respective parameter obtained from the entire sample population under study


## 🤖 5. Damage Classification Model (CNN + YOLO)

Deep learning pipeline including:

- **Convolutional Neural Network (CNN)**
- **YOLO object detection**

Classes detected:

- Healthy  
- Pathogenic Damage  
- Physiological Damage  
- Mechanical Damage  

This allows **automatic postharvest defect detection** from RGB images.

---

## 🧪 Purpose

This repository supports a **multi-scale, multi-sensor analytical ecosystem** for carrot quality:

- Nutritional profiling  
- Phenological monitoring  
- Physiological evaluation  
- Damage detection  
- Spectral and RGB-based carotenoid estimation  

Data sources include **RGB images, multispectral drone orthomosaics, and laboratory VIS–NIR spectra**, combined with **AI modeling**.

---

# 📘 Dictionary of Variables (English)

Below is a unified dictionary of common variables used across the four Jupyter notebooks:

---

## 🎨 **Color Index & CIELAB Variables**
| Variable | Description |
|---------|-------------|
| `L` or `L*` | Lightness component (0 = black, 100 = white) |
| `a` or `a*` | Green–red chromatic axis (+a* = red, −a* = green) |
| `b` or `b*` | Blue–yellow chromatic axis (+b* = yellow, −b* = blue) |
| `ICarot` | Custom carotenoid-sensitive index derived from L*, a*, b* |
| `Hue` | Color angle, indicator of pigment composition |
| `Chroma` | Color saturation or purity |
| `IC` | Image-based carotenoid index (generic) |

---

## 🌾 **Spectral & UAV Variables**
| Variable | Description |
|---------|-------------|
| `NDVI` | Normalized Difference Vegetation Index |
| `GNDVI` | Green NDVI, sensitive to chlorophyll |
| `NDRE` | Red-edge NDVI, sensitive to stress and pigments |
| `SAVI` | Soil-adjusted vegetation index |
| `OSAVI` | Optimized SAVI |
| `MCARI` | Modified Chlorophyll Absorption Ratio Index |
| `TCARI` | Transformed Chlorophyll Absorption Ratio Index |
| `CIgreen`, `CIrededge` | Chlorophyll indices |
| `Reflectance (%)` | Spectral reflectance from VIS–NIR measurements |
| `Wavelength` | Spectral band position in nanometers |

---

## 🧪 **Laboratory & Physiological Variables**
| Variable | Description |
|---------|-------------|
| `Carot_tot` | Total carotenoid content (mg/100g fw) |
| `FW` | Fresh weight |
| `DW` | Dry weight |
| `Respiration` | CO₂ production rate (indicator of physiological status) |
| `Firmness` | Texture measured by penetration force (N) |
| `Solubles` / `TSS` | Total soluble solids (°Brix) |
| `pH` | Acidity level |
| `TA` / `ATT` | Titratable acidity |

---

## 🥕 **Damage Classification Variables**
| Variable | Description |
|---------|-------------|
| `Damage_class` | Assigned class label (Healthy, Mechanical, Pathogenic, Physiological) |
| `Bounding_box` | YOLO detection coordinates |
| `Conf_score` | Confidence score of detection |
| `Img_ID` | Image identifier |
| `CNN_pred` | Prediction output of CNN model |

---

## 🧠 **Modeling & ML Variables**
| Variable | Description |
|---------|-------------|
| `X` | Input feature matrix |
| `y` | Target variable |
| `y_pred` | Model prediction |
| `RMSE` | Root Mean Squared Error |
| `MAE` | Mean Absolute Error |
| `R2` | Coefficient of determination |
| `Train_set`, `Test_set` | Training and testing partitions |
| `Scaler` | Normalization object (StandardScaler, MinMaxScaler) |
| `Feature_importance` | Importance ranking of input variables |

---

# 📜 Citation and Responsible Use

Anyone using the **datasets, models, scripts, or methodologies** from this repository **must cite**:

- The SGR Project:  
  **“Strengthening the Carrot Production Chain” (BPIN 2020000100192)**  
- The corresponding scientific article (Citation will be added upon publication)

---

# ⭐ Provisional Citation

> *Predictive Modeling of Carotenoid Content and Damage Classification in Carrots Using Spectral Techniques, Colorimetry, and Artificial Intelligence*.  
> SGR Project BPIN 2020000100192.

---

