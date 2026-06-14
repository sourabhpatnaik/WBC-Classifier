# 🧬 HemoVision AI — White Blood Cell Classifier

![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

> An intelligent diagnostic web application that classifies **White Blood Cells (WBCs)** from microscopic blood smear images using classical machine learning — achieving **87.50% accuracy** with Random Forest.

---

## 🔬 Project Overview

HemoVision AI automates leukocyte morphology classification from raw microscopy images. The system preprocesses blood smear samples, extracts pixel-level features, and runs them through a trained ML pipeline to predict the WBC type along with confidence probabilities.

The model classifies cells into **4 leukocyte categories**:

| Cell Type | Role |
|-----------|------|
| 🟣 **Eosinophil** | Fights parasitic infections & allergies |
| 🔵 **Lymphocyte** | Key to adaptive immune response |
| 🟢 **Monocyte** | Largest WBC, differentiates into macrophage |
| 🟡 **Neutrophil** | First responder to bacterial infection |

---

## 🚀 Live Demo

🔗 **[HemoVision AI — Streamlit App](#):** *https://wbc-classifier.streamlit.app*

---

## 🖥️ App Features

- **🔍 Predict Blood Cell** — Upload a JPG/PNG blood smear image and get instant WBC classification with confidence scores and per-class probability breakdown
- **📌 Project Overview** — Full pipeline explanation, tech stack, and key results
- **📊 Dataset & EDA** — Class distribution, preprocessing visualization, and pixel intensity analysis
- **🤖 Model Evaluation** — Accuracy comparison, confusion matrices, and classification reports for KNN, SVM, and Random Forest

---

## ⚙️ ML Pipeline

```
Blood Smear Image (JPG/PNG)
        ↓
Preprocessing → Resize to 64×64 → Grayscale Conversion
        ↓
Feature Extraction → Flatten pixel values → 4096 features
        ↓
Normalization → MinMaxScaler [0, 1]
        ↓
ML Classification → Random Forest (Best Model)
        ↓
Prediction → Class Label + Confidence Probabilities
```

---

## 📊 Model Performance

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| KNN | 64.25% | 0.56 | 0.55 | 0.55 |
| SVM | 81.25% | 0.77 | 0.76 | 0.76 |
| **Random Forest ⭐** | **87.50%** | **0.87** | **0.87** | **0.87** |

### 🏆 Why Random Forest?
- **Ensemble Power** — Combines 100+ decision trees to reduce overfitting and variance
- **High-Dimensional** — Handles 4096 pixel features efficiently without scaling issues
- **Class Balance** — Maintains strong boundaries over symmetric sample sizes
- **Best Metrics** — 87.50% accuracy, 0.87 macro F1 across all 4 WBC classes

---

## 🗂️ Dataset

| Property | Detail |
|----------|--------|
| Total Images | 2,000 |
| Classes | 4 (Eosinophil, Lymphocyte, Monocyte, Neutrophil) |
| Samples per Class | 500 (perfectly balanced) |
| Image Size | 64 × 64 px (grayscale) |
| Train / Test Split | 80% / 20% |
| Format | JPG (microscopy imagery) |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.x | Core language |
| OpenCV | Image preprocessing |
| scikit-learn | ML models & evaluation |
| NumPy / Pandas | Data processing |
| Matplotlib / Seaborn | Visualization |
| Streamlit | Web deployment |
| Joblib | Model serialization |

---

## 📁 Project Structure

```
HemoVision-AI/
│
├── app.py                  # Main Streamlit application
├── Model/
│   └── WBC_Model.pkl       # Trained pipeline (model + scaler + encoder)
├── requirements.txt        # Python dependencies
└── README.md
```

---

## ⚡ Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/sourabhpatnaik/WBC-Classifier.git
cd WBC-Classifier
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the app**
```bash
streamlit run app.py
```

---

## 📦 Requirements

```
streamlit
opencv-python
scikit-learn
numpy
pandas
matplotlib
seaborn
joblib
Pillow
```

---

## 👤 Author

**Sourabh Patnaik**
- GitHub: [@sourabhpatnaik](https://github.com/sourabhpatnaik)
- B.Tech in Computer Science (Gaming Technology) — VIT Bhopal

---

*Built as part of the Data Science Program at Innomatics Research Labs*
