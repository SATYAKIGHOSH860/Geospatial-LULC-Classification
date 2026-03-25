# 🛰️ Geospatial Land Use Classification using Sentinel-2

##  Overview

This project implements a **Land Use / Land Cover (LULC) classification system** using **multispectral Sentinel-2 satellite imagery**.

The system classifies images into:

* Urban
* Water
* Vegetation
* Barren

---

##  Objectives

* Use multispectral satellite data instead of RGB
* Apply deep learning (CNN) for classification
* Integrate domain-specific features like NDVI
* Evaluate performance using multiple metrics

---

##  Dataset

* Dataset: EuroSAT (Sentinel-2)
* Bands used:

  * B2 (Blue)
  * B3 (Green)
  * B4 (Red)
  * B8 (NIR)

Dataset is not uploaded due to size. Use:
https://zenodo.org/records/7711810

---

##  Methodology

### 1. Data Preprocessing

* Loaded multispectral `.tif` images
* Selected relevant bands (B2, B3, B4, B8)
* Normalized pixel values

### 2. Feature Engineering

NDVI (Normalized Difference Vegetation Index):

NDVI = (NIR - Red) / (NIR + Red)

### 3. Model

* Convolutional Neural Network (CNN)
* Input shape: (64, 64, 5)
* Layers:

  * Conv2D → MaxPooling
  * Conv2D → MaxPooling
  * Conv2D → Flatten
  * Dense → Output

---

##  Results

* Training Accuracy: ~95%
* Validation Accuracy: ~92–93%

### Confusion Matrix Insights:

* Strong performance on Vegetation and Water
* Moderate confusion between Barren and Urban classes

---

##  Evaluation Metrics

* Accuracy
* Confusion Matrix
* Precision / Recall / F1-score

---

##  Sample Predictions

(See results/sample_predictions.png)

---

##  Tech Stack

* Python
* TensorFlow / Keras
* NumPy
* Rasterio
* Matplotlib
* Scikit-learn

---

##  Future Improvements

* Add NDBI for better urban/barren classification
* Use additional spectral bands (SWIR)
* Implement UNet for segmentation
* Integrate Google Earth Engine for real-time data

---

##  Author
Satyaki Ghosh  
M.Tech AI & Data Science Student  

Project aligned with ISRO/NESAC internship domains.
