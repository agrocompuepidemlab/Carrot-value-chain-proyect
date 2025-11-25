# 🥕 Predictive Modeling for Carrot Quality, Carotenoid Content, and Damage Classification  
### Chapter 3 — Spectral Techniques, Colorimetry & Artificial Intelligence

This repository contains the code used in **Chapter 3: _Predictive modeling of carotenoid content and damage classification in carrots using spectral techniques, colorimetry, and AI_**, developed within the SGR-funded project:

**“Strengthening the Carrot Production Chain” (BPIN 2020000100192)**.

---

## 📡 Overview of Models and Analytical Pipelines

This repository integrates multiple machine-learning, spectral, and imaging workflows for carrot quality assessment under field and laboratory conditions.

### 🌱 **1. Phenology Classification Model (UAV Orthomosaics)**  
A machine-learning model trained on **spectral indices extracted from drone-based multispectral orthomosaics** to classify carrot crop phenological stages.

### 🌈 **2. Carotenoid Regression Model From Orthomosaics**  
A regression framework for **estimating carotenoid content directly from spectral vegetation indices obtained from UAV imagery**, enabling non-destructive biochemical approximation at field scale.

---

## 🔬 **3. High-Resolution Carotenoid Model From Spectroradiometer Signatures**

A regression model built using **VIS–NIR spectral signatures (350–2500 nm)** collected with a **Spectral Evolution field spectroradiometer**.  
This model provides fine biochemical estimation of carotenoids through feature extraction and multivariate modeling.

---

## 🎨 **4. RGB-Based Carotenoid Estimation Using a Custom Color Index (ICcarot)**

An image-based carotenoid prediction pipeline derived from:

- Extraction of **CIELAB color features (L*, a*, b*)**
- Computation of the custom pigment-sensitive index **ICcarot**, defined as:

\[
IC_{carot} = 0.7\left(\frac{b^*}{b^*_{max}}\right) + 
             0.2\left(\frac{a^*}{a^*_{max}}\right) + 
             0.1\left(\frac{C^*}{C^*_{max}}\right)
\]

This index was calibrated with laboratory carotenoid measurements to classify samples into:

- **Low carotenoid content**
- **Medium carotenoid content**
- **High carotenoid content**

and to support image-based regression models.

---

## 🤖 **5. Damage Classification Model (CNN + YOLO)**

A deep-learning pipeline integrating:

- A **Convolutional Neural Network**  
- A **YOLO object detection model**  

to classify carrot roots into:

- **Healthy**
- **Pathogenic damage**
- **Physiological damage**
- **Mechanical damage**

This enables automated visual inspection and defect detection from RGB images captured during postharvest evaluation.

---

## 📁 Repository Contents

- `data/` – Color, spectral and chemical reference datasets  
- `models/` – Trained model weights and pipelines  
- `notebooks/` – Jupyter notebooks for training, evaluation and visualization  
- `src/` – Image processing, spectral analysis and ML utilities  
- `README.md` – Project overview  

---

## 🧪 Purpose

This repository supports a **multi-scale, multi-sensor approach** for:

- Nutritional profiling  
- Physiological evaluation  
- Damage detection  
- Phenological monitoring  

combining  
**RGB**, **multispectral orthomosaics**, **field spectroradiometry**, and **AI modeling**.

---

## ⭐ Citation

If you use this repository, please cite:

> _Chapter 3 – Predictive Modeling of Carotenoid Content and Damage Classification in Carrots Using Spectral Techniques, Colorimetry, and AI_  
> SGR Project BPIN 2020000100192.

---

