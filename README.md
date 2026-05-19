# ML4SCS — Group Gruppenraum 3

## Project Overview
This repository contains our semester-long group project for **Applied Machine Learning for Smart and Connected Systems (ML4SCS)** at Leuphana Universität Lüneburg (SoSe 2026).

The goal is to build a complete machine learning pipeline that recognizes **air-written digits (0–9)** using motion sensor data from a smartphone.

Full project workflow:
- Data collection via Phyphox (Accelerometer + Gyroscope)
- Preprocessing and feature extraction
- Model training (Random Forest)
- Evaluation and iteration
- Final conclusions

---

## Team Members
- **Isa Kilic** (Team Captain)
- **Efe Özüm**
- **Tony Duong**

---

## Research Question
Can hand-written digits (0–9) drawn in the air be recognized using motion sensor data (accelerometer and gyroscope) from a smartphone, and how accurately can a machine learning model classify them?

---

## Dataset
- **Dataset name:** Air-Writing Digit Dataset (self-recorded)
- **Source:** Phyphox app on smartphone (recorded by team members)
- **Type of data:** Time-series sensor data — Accelerometer (m/s²) and Gyroscope (rad/s)
- **Target variable:** Digit class (0–9)
- **Features:** 24 statistical features per recording (mean, std, max, min for each of 6 sensor axes)

---

## Project Structure
```
├── dummy_data/          # Synthetic test recordings
├── real_data/           # Real sensor recordings (Phyphox)
├── notebooks/           # Jupyter notebooks
├── reports/             # Weekly progress reports
│   ├── week01.md
│   ├── week02.md
│   ├── week03.md
│   └── week04.md
├── src/
│   ├── preprocessing.py     # Feature extraction pipeline
│   ├── train.py             # Model training (Random Forest)
│   ├── predict.py           # Prediction for new recordings
│   ├── evaluate.py          # Model evaluation
│   └── plot_recordings.py   # Data visualisation
└── requirements.txt
```

---

## How to Run

**1. Install dependencies:**
```bash
pip install pandas numpy scikit-learn matplotlib scipy joblib
```

**2. Record data with Phyphox:**
- Use "Linear Acceleration" experiment
- Export as CSV → place in `real_data/digit_X_runXX/`

**3. Train the model:**
```bash
python src/train.py
```

**4. Predict a new recording:**
```bash
python src/predict.py
```

---

## Current Status
| Digit | Recordings | Status |
|-------|-----------|--------|
| 0 | 0 | ⏳ Pending |
| 1 | 0 | ⏳ Pending |
| 2 | 0 | ⏳ Pending |
| 3 | 10 | ✅ Done |

---

## Supervisor
Prof. Burkhardt Funk — Leuphana Universität Lüneburg