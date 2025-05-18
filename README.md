# Aegis: Real-Time Cardiac Event Forecasting System
*Built by Anova Youngers under Parthegon Health*

**"Because the heart doesn't always warn twice."**

---

## Overview

**Aegis** is a survival modeling system designed to predict imminent cardiac events using deep learning and time-to-event analysis. It combines high-resolution waveform data (MIMIC-IV) with simulated symptom logs and vitals to generate dynamic risk forecasts—empowering patients and clinicians with early alerts in the critical minutes before a cardiac crisis.

This project demonstrates how survival models (e.g., DeepSurv, Cox, XGBoost-Surv) can be applied to real-time health monitoring systems, with the goal of integrating into dashboards or IoT-connected wearables.

---

## Features

- Real-time **probabilistic forecasting** for cardiac events
- Integration with **MIMIC-IV Waveform** data and symptom trajectories
- Dynamic **time-to-event survival modeling** using PySurvival & DeepSurv
- ECG, HRV, SpO₂ signal alignment with event metadata
- **Synthetic patient simulation engine** for testing early warning scenarios
- Clean modular design for extensibility into:
  - Wearable device ingestion
  - Alerting thresholds
  - Dashboard visualizations

---

## Technologies Used

- AWS SageMaker (dev environment)
- Python, Pandas, NumPy
- WFDB, PySurvival, Lifelines
- MIMIC-IV Waveform dataset (via PhysioNet + BigQuery)
- JupyterLab, Matplotlib/Plotly (for signal & risk curve visualization)

---

## Project Structure

aegis-survival-lab/
│
├── data/
│   ├── raw/              # Raw ECG, HR, SpO2 waveform files
│   ├── processed/        # Cleaned, aligned patient timeseries
│   └── simulated/        # Synthetic patient trajectories
│
├── notebooks/
│   ├── 01_download_waveforms.ipynb
│   ├── 02_symptom_simulation.ipynb
│   ├── 03_deepsurv_modeling.ipynb
│   └── 04_survival_forecasting_demo.ipynb
│
├── scripts/
│   ├── fetch_mimic_waveforms.py
│   ├── simulate_patients.py
│   └── train_survival_model.py
│
├── README.md
└── requirements.txt

---

## Getting Started

1. **Clone the repo**  
```bash
git clone https://github.com/AnovaYoung/aegis
cd aegis

	2.	Install dependencies

pip install -r requirements.txt

	3.	Download waveform segments
Use fetch_mimic_waveforms.py or run the notebook to extract aligned ECG, HR, and SpO₂ data around cardiac events.
	4.	Simulate symptom patterns

python scripts/simulate_patients.py

	5.	Train survival model
Run train_survival_model.py or use 03_deepsurv_modeling.ipynb.

⸻

Status

Actively in development. Phase 1 will complete with a working survival model trained on synthetic and real waveform-aligned data.

⸻

Future Work
	•	Real-time risk scoring dashboard
	•	LLM integration for patient-reported symptom parsing
	•	Mobile app / wearable data ingestion
	•	Transfer learning from ICU to outpatient settings

⸻

License

MIT License

⸻

Contact

Anova Youngers
GitHub: @AnovaYoung
Email: m.anovayoungers@gmail.com
LinkedIn: in/m-anova-youngers

⸻

Parthegon Health – Precision AI for Preventive Cardiac Care.
