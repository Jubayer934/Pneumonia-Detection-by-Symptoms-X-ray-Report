
## **Pneumonia Detection using Symptoms + Chest X-ray**  
> **এক ক্লিকে শ্বাসের নিরাপত্তা**  
> *One-click breath safety — powered by Dual AI (VGG16 + SVC)* 

---

## Overview

**শ্বাসAI** is a **dual-input AI system** for early **pneumonia detection** in Bangladesh, combining:

| Input Type       | Model Used         | Purpose |
|------------------|--------------------|--------|
| **Chest X-ray**  | **VGG16 (CNN)**    | Image classification (Pneumonia / Normal) |
| **Patient Data** | **SVC (SVM)**      | Tabular classification (Symptoms, vitals) |

Both models run **independently**, then **combine confidence scores** to give a **final verdict** with **PDF report**.

---

## Features

- **Dual AI Prediction** (Image + Clinical)
- **Interactive Web UI** (Colab / Streamlit)
- **Auto-generated PDF Report** (Bangla + English)
- **Handles missing data** (median / 'Unknown')
- **One-click download**
- **Bangla UI support**
- **Deployable on Android, Web, Clinic PACS**

---

## Models

| Model | Architecture | Input | Output |
|------|--------------|-------|--------|
| **Image Model** | `VGG16` (pre-trained) + Custom Head | 224×224 RGB X-ray | Pneumonia (0/1) |
| **Tabular Model** | `SVC` (RBF kernel) | 12 clinical features | Pneumonia (0/1) |

> Trained on **Kaggle Chest X-ray** 

---

## Project Structure
Pneumonia Detection using Symptoms + Chest X-ray/ <br>
├── pneumonia_Image.ipynb         # Classification image <br>
├── pneumonia_tabuluer.ipynb      # Classification tabuluer data <br>
├── data/ <br>
│   └── sample_xray.jpg-------------# Test image <br>
├── reports/ <br>
│   └── Pneumonia_Report.pdf------------# Example output <br>
└── README.md <br>

---

## Project Structure

[Tabuluer Dataset](https://www.kaggle.com/datasets/essienmary/pneumonia-dataset) <br>
[Image Dataset](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)