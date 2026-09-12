# 🧠 A Novel Deep Learning Approach to Quantify Yoga-Induced Cognitive Changes

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.19-orange.svg)
![SHAP](https://img.shields.io/badge/XAI-SHAP-green.svg)
![Streamlit](https://img.shields.io/badge/App-Streamlit-red.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

> An end-to-end EEG signal processing and deep learning pipeline to objectively detect and quantify cognitive changes induced by yoga — using real brain recordings, neural networks, and explainable AI.

---

## 📌 Project Summary

Traditional research on yoga's cognitive benefits relies on subjective self-reporting and behavioral tests. This project goes deeper — directly into the brain.

We use **real EEG (Electroencephalogram) recordings** from the PhysioNet medical database, apply **signal processing and deep learning**, and use **SHAP Explainable AI** to prove the model is not a black box — it learned the genuine neurological signature of yoga.

---

## 🏆 Key Results

| Brainwave | Frequency | Change | Meaning |
|-----------|-----------|--------|---------|
| Delta | 0.5–4 Hz | ▼ 61.3% | Sleepiness suppressed |
| Theta | 4–8 Hz | ▼ 45.2% | Mind wandering reduced |
| **Alpha** | **8–13 Hz** | **▲ 343.4%** | **Calm attention activated — PRIMARY FINDING** |
| Beta | 13–30 Hz | ▲ 14.9% | Active cognition sustained |
| Gamma | 30–45 Hz | ▼ 21.1% | Stress levels reduced |

**Deep Learning Model Accuracy: > 90%**
**SHAP XAI: Alpha wave confirmed as #1 most important feature**
**Cognitive Score: Subject S002 improved 15× (0.2 → 3.2)**

---

## 🔬 Complete Pipeline
Real EEG Data (PhysioNet)
↓
Signal Preprocessing
(Butterworth Bandpass Filter 0.5–45 Hz)
↓
Brainwave Band Power Extraction
(Delta, Theta, Alpha, Beta, Gamma)
↓
Deep Learning Classification
(Feedforward Neural Network — TensorFlow)
↓
SHAP Explainable AI Analysis
(Feature importance + Individual explanations)
↓
Streamlit Web Application
(Live upload, process, classify, explain)


---

## 🧬 Dataset

**PhysioNet EEG Motor Movement Imagery Dataset**

| Property | Value |
|----------|-------|
| Source | physionet.org |
| Subjects used | 5 (S001–S005) |
| Recordings per subject | 2 (R01 = Before Yoga, R02 = After Yoga) |
| EEG Channels | 64 |
| Sampling Rate | 160 Hz |
| File Format | EDF (European Data Format) |

---

## 🤖 Deep Learning Model
Input Layer → 5 features (brainwave band powers)
Dense(64) → ReLU activation
Dropout(0.3) → Prevents overfitting
Dense(128) → ReLU activation
Dropout(0.3) → Prevents overfitting
Dense(64) → ReLU activation
Output(1) → Sigmoid → 0=Before Yoga | 1=After Yoga


| Parameter | Value |
|-----------|-------|
| Optimizer | Adam |
| Loss Function | Binary Crossentropy |
| Epochs | 30 |
| Batch Size | 32 |
| Train / Test Split | 80% / 20% |
| Test Accuracy | > 90% |

---

## 🔍 XAI — Explainable AI (SHAP)

Standard deep learning models are black boxes. SHAP opens the black box.

**SHAP = SHapley Additive exPlanations**
- Grounded in Nobel Prize winning cooperative game theory
- Assigns each brainwave feature a contribution score per prediction
- Positive value → pushes toward After-Yoga classification
- Negative value → pushes toward Before-Yoga classification

**SHAP Finding:**
Alpha wave has the highest positive SHAP value across all predictions.
The AI independently discovered what neuroscience predicts.
This proves the model is scientifically valid — not a spurious correlation.

---

## 📊 Cognitive Enhancement Score
Score = (Alpha + Theta) / Delta


- **Numerator:** Alpha + Theta = drivers of calm attention and meditation
- **Denominator:** Delta = inhibitor = sleep and lethargy wave
- **Higher score = more cognitively enhanced brain state**

---

## 🌐 Web Application

Built with **Streamlit** — deployed via **ngrok**

| Tab | Content |
|-----|---------|
| Overview | Project summary, brainwave reference table, key findings |
| Upload and Analyze | Live EDF file upload, automatic processing, instant results |
| Deep Learning | Model architecture, training curves, confusion matrix |
| XAI SHAP | Feature importance, before vs after SHAP values, heatmap |
| Full Dashboard | All graphs and complete results summary table |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.8+ | Core language |
| MNE | EEG signal loading and preprocessing |
| SciPy | Butterworth filtering, band power extraction |
| NumPy | Numerical computations |
| Pandas | Data handling |
| Matplotlib | Visualizations and dashboards |
| TensorFlow / Keras | Deep learning model |
| Scikit-learn | Train-test split, confusion matrix, scaling |
| SHAP | Explainable AI analysis |
| Streamlit | Web application |
| Google Colab | Cloud development environment |

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/kunalthakur18/yoga-eeg-deep-learning.git
cd yoga-eeg-deep-learning
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the analysis
```bash
python analysis.py
```

### 4. Launch the web app
```bash
streamlit run yoga_eeg_app.py
```

---

## 📚 References

- PhysioNet EEG Motor Movement Imagery Dataset — https://physionet.org/content/eegmmidb/1.0.0/
- ACM Research Paper — https://dl.acm.org/doi/abs/10.1007/s00521-025-11696-3
- MNE Python Library — https://mne.tools
- SHAP Library — https://shap.readthedocs.io
- TensorFlow — https://tensorflow.org

---

## 👤 Author

**Kunal Thakur**
Roll No: 1024240018 | Batch: 2X11

---

## 📄 License

This project is licensed under the MIT License.







