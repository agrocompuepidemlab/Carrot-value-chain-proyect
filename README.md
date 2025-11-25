# 🥕 Predictive Modeling for Carrot Quality, Carotenoid Content, and Damage Classification  
### Article — Spectral Techniques, Colorimetry & Artificial Intelligence

This repository contains the code used in the **article on predictive modeling of carotenoid content and damage classification in carrots using spectral techniques, colorimetry, and artificial intelligence**, developed within the SGR-funded project:

**“Strengthening the Carrot Production Chain” (BPIN 2020000100192)**.

---

## 📡 Overview of Models and Analytical Pipelines

This repository integrates multiple machine-learning, spectral, and imaging workflows for carrot quality assessment under field and laboratory conditions.

---

## 🌱 **1. Phenology Classification Model (UAV Orthomosaics)**  
A machine-learning model trained on **spectral indices extracted from drone-based multispectral orthomosaics** to classify carrot crop phenological stages.

---

## 🌈 **2. Carotenoid Regression Model From Orthomosaics**  
A regression model for **estimating carotenoid content directly from spectral vegetation indices obtained from UAV orthomosaics**, enabling non-destructive biochemical approximation under field conditions.

---

## 🔬 **3. High-Resolution Carotenoid Model From Laboratory Spectroradiometer Signatures**

A regression model built using **VIS–NIR spectral signatures (350–2500 nm)** acquired **in laboratory conditions** using a **Spectral Evolution spectroradiometer**.  
Spectral measurements were collected under controlled illumination and geometry, ensuring high-fidelity reflectance data for precise carotenoid estimation.

---

## 🎨 **4. RGB-Based Carotenoid Estimation Using a Custom Color Index (ICcarot)**

An RGB image-based carotenoid prediction workflow derived from:

- Extraction of **CIELAB color features** (L*, a*, b*)  
- Computation of a custom pigment-sensitive index **ICarot**, defined as:

\[
IC_{carot} = 0.7\left(\frac{b^*}{b^*_{max}}\right) + 
             0.2\left(\frac{a^*}{a^*_{max}}\right) + 
             0.1\left(\frac{C^*}{C^*_{max}}\right)<img width="990" height="322" alt="image" src="https://github.com/user-attachments/assets/9c042cef-5edf-423b-ba42-1627ebd02190" />

\]

The index was calibrated using laboratory carotenoid data to classify samples into:

- **Low carotenoid content**
- **Medium carotenoid content**
- **High carotenoid content**

and to support RGB-based regression models.

---

## 🤖 **5. Damage Classification Model (CNN + YOLO)**

A deep-learning pipeline integrating:

- A **Convolutional Neural Network**, and  
- A **YOLO object detection model**

to classify carrot roots into:

- **Healthy**
- **Pathogenic Damage**
- **Physiological Damage**
- **Mechanical Damage**

This system enables automated visual inspection and defect detection from RGB images captured during postharvest evaluation.

---

## 🧪 Purpose

This repository supports a **multi-scale, multi-sensor approach** for:

- Nutritional profiling  
- Phenological monitoring  
- Physiological assessment  
- Damage detection  

combining **RGB imaging**, **multispectral drone orthomosaics**, **laboratory spectroradiometry**, and advanced **AI modeling**.

---

## 📜 Citation and Responsible Use

Anyone using the **datasets, models, scripts, or methodologies** in this repository **must cite and acknowledge the original source**, including:

- The SGR project:  
  **“Strengthening the Carrot Production Chain” (BPIN 2020000100192)**  
- The corresponding scientific article associated with this repository  

Failure to cite constitutes improper academic and scientific use.

A formal citation will be added once the article is published.

---

## ⭐ Provisional Citation

> _Predictive Modeling of Carotenoid Content and Damage Classification in Carrots Using Spectral Techniques, Colorimetry, and AI_.  
> SGR Project BPIN 2020000100192.

---

