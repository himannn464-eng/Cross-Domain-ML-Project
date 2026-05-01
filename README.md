# Cross-Domain Explainable ML Framework

A trustworthy machine learning project that compares model behavior across **two very different real-world domains**:

- **Breast cancer histopathology image classification**
- **Phishing website detection**

Instead of focusing only on accuracy, this project studies **generalization, explainability, and robustness** across computer vision and cybersecurity tasks in a single unified framework.

---

## Project Overview

Most machine learning projects solve one problem in one domain. This project goes beyond that by asking:

- Can a common evaluation mindset work across **medical imaging** and **cybersecurity**?
- How do different models behave under **perturbations and noisy conditions**?
- Can predictions be made more **trustworthy and interpretable**?

To answer these questions, the project combines:

- A **ResNet50-based CNN** for breast cancer image classification
- A **Random Forest classifier** for phishing website detection
- Explainability methods to understand predictions
- Robustness testing to evaluate reliability beyond clean benchmark performance

This makes the project closer to **real applied ML systems**, where trust and reliability matter as much as raw metrics.

---

## Why This Project Stands Out

- Solves problems in **two unrelated domains** using a unified ML evaluation perspective
- Combines **deep learning + classical machine learning** in one repository
- Focuses on **trustworthy AI**, not just prediction accuracy
- Includes **interpretability and robustness analysis**
- Demonstrates practical skills in:
  - computer vision
  - tabular machine learning
  - healthcare AI
  - cybersecurity analytics
  - reproducible ML workflows

---

## Domains Covered

### 1. Breast Cancer Histopathology Detection
This module classifies breast histopathology images into binary classes using a CNN pipeline based on **ResNet50**.

**Goal:** Detect patterns associated with benign and malignant tissue samples.

**Dataset:** BreaKHis

**Approach:**
- Image preprocessing and resizing
- Transfer learning using ResNet50
- Binary classification pipeline
- Confidence-based prediction output

**Explainability focus:**
- Visual reasoning support using interpretation techniques
- Important patterns observed include **nuclei density** and **glandular disruption**

---

### 2. Phishing Website Detection
This module predicts whether a website is **phishing** or **legitimate** using a **Random Forest classifier** trained on handcrafted website and URL-based features.

**Goal:** Detect suspicious websites from structured feature inputs.

**Input includes 30 phishing-related features such as:**
- `having_IP_Address`
- `URL_Length`
- `SSLfinal_State`
- `Request_URL`
- `Google_Index`
- `Links_pointing_to_page`

**Approach:**
- Tabular feature preprocessing
- Random Forest training
- Feature-based inference
- Demo prediction using a full 30-feature sample

**Interpretability focus:**
- Feature importance analysis
- Strong indicators include **IP address usage**, **URL length**, and **SSL-related signals**

---

## Core Idea

The central contribution of this work is a **cross-domain trustworthy ML framework**.

Rather than treating healthcare and cybersecurity as separate projects, this repository studies how to build and evaluate models under a common framework using:

- prediction performance
- explainability
- robustness testing
- domain-specific interpretation

This creates a more realistic view of how ML models behave in the real world.

---

## Robustness Analysis

A key part of this project is evaluating how models perform when conditions are no longer ideal.

Instead of reporting only clean-data performance, this project also examines how accuracy-related behavior changes under perturbations.

### Observed robustness drops
- **Breast CNN:** 7.2% performance drop under perturbation
- **Phishing RF:** 5.8% performance drop under perturbation

This helps assess whether a model is only benchmark-friendly or actually dependable under practical conditions.

---

## Models Used

| Domain | Model | Input Type | Objective |
|--------|-------|------------|-----------|
| Breast Cancer Detection | ResNet50-based CNN | Histopathology Images | Binary classification |
| Phishing Detection | Random Forest | Tabular Website Features | Binary classification |

---

## Tech Stack

- **Python**
- **PyTorch**
- **TensorFlow / Keras**
- **Scikit-learn**
- **NumPy**
- **Pandas**
- **Joblib**
- **SHAP**
- **Grad-CAM**
- **Matplotlib / Seaborn**

---

## Repository Structure

```text
Cross-Domain-ML-Project/
│
├── breast_pipeline.py
├── phishing_pipeline.py
├── demo_prediction.py
├── requirements.txt
├── README.md
│
├── outputs_breast/
├── outputs_phishing/
├── sample_breast_image.png
└── ...
```

---

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/sahkanishk01/Cross-Domain-ML-Project.git
cd Cross-Domain-ML-Project
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run demo prediction

```bash
python demo_prediction.py
```

---

## Demo Capabilities

The demo script performs prediction for both domains:

### Breast Cancer Demo
- Loads the trained breast cancer model
- Takes a sample histopathology image
- Outputs:
  - predicted class
  - confidence score

### Phishing Demo
- Loads the trained phishing detection model
- Uses a 30-feature phishing sample
- Outputs:
  - predicted class
  - phishing/legitimate decision

---

## Example Project Value for Recruiters

This project demonstrates the ability to:

- build ML systems across **multiple domains**
- work with both **images and structured data**
- apply both **deep learning and traditional ML**
- handle **model inference pipelines**
- think beyond training accuracy by including:
  - robustness analysis
  - interpretability
  - deployment-ready demo prediction

It reflects practical readiness for roles in:

- Machine Learning Engineer
- Data Scientist
- Computer Vision Engineer
- Applied AI Engineer
- Cybersecurity Analytics / ML roles
- Healthcare AI research

---

## Key Learning Outcomes

Through this project, the following skills were developed and applied:

- Transfer learning with CNNs
- Binary classification for medical images
- Feature-based phishing detection
- End-to-end ML pipeline design
- Trustworthy AI concepts
- Explainability in ML systems
- Robustness-oriented evaluation
- Reproducible project structuring

---

## Future Improvements

- Add a **Streamlit or Flask web app** for live predictions
- Add visual explainability outputs directly in the demo
- Store model metadata using model cards
- Add automated evaluation scripts
- Expand robustness testing with adversarial or noisy inputs
- Include richer experiment tracking and result dashboards

---

## Author

**Kanishk Sah**  
Final Year Project  
Cross-Domain Explainable ML Framework

---

## License

This project is intended for academic, learning, and portfolio purposes.

If you want to make it open for reuse, add an **MIT License** file to the repository.
