## 🧠 Fall & Near-Fall Detection from Wearable Sensor Data

This project applies machine learning and classical signal processing to detect **falls, near-falls, and daily activities** using **wearable IMU, ECG, and GSS sensor data** collected at 1000Hz.

---

### 💡 Project Overview

Falls are a major health concern among older adults, often leading to injury and hospitalization. My goal was to create a robust pipeline that can **detect and distinguish falls and near-falls** in real-time, using data from wearable sensors.

The project was completed as part of the UBC Biomedical Engineering "400K Grand Challenge".

---

### 🛠️ Core Contributions

#### 📈 Data Processing Pipeline

- Developed a reusable end-to-end pipeline:
  - Filtering raw sensor data
  - Segmenting based on event timing
  - Windowing into 1.5s overlapping segments
  - Feature extraction for IMU, ECG, and GSS data
  - Labeling based on event overlap (Fall, Near-Fall, ADL)

#### 🧪 Feature Engineering

- Extracted 84+ classical time and frequency domain features per sensor
- Included HRV-specific features for ECG and gait-specific metrics from GSS
- Treated IMU data as position-agnostic to improve generalizability

#### 🤖 Machine Learning & Evaluation

- Trained Random Forest models for:
  - Stage 1: ADL vs Non-ADL
  - Stage 2: Fall vs Near-Fall
- Achieved:
  - **83% accuracy** for ADL vs Non-ADL
  - **Stage 2 ensemble models** for fall classification
- Addressed class imbalance and sensor variance

#### 🔬 Validation

- Designed pipeline to support per-participant validation
- Evaluated model on independent participant (P3033) to simulate unseen deployment

---

### 🧠 Skills Demonstrated

- Signal processing (filtering, segmentation)
- Feature engineering for time-series data
- Classical ML (Random Forest, ensemble models)
- Model evaluation (participant-wise validation)
- Python (NumPy, Pandas, Scikit-learn, Matplotlib)
- Scientific documentation and reproducible pipelines

---

### ✅ Requirements

```bash
pip install numpy pandas scikit-learn matplotlib scipy
```
