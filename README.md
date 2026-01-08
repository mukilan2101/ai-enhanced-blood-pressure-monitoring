# AI-Enhanced Blood Pressure Monitoring System

Clinical-grade ML system for cuffless blood pressure prediction and CVD risk estimation.

## 🧰 Tech stack
- Python, Scikit-learn
- Signal processing (Butterworth bandpass, zero-phase filtering, noise reduction)
- MIMIC III dataset
- Docker, MLflow, AWS

## ✨ Features
- Predicts systolic blood pressure and CVD risk from physiological signals.
- Robust preprocessing pipeline for noisy clinical data.
- Automated training, evaluation, and model versioning scripts.

## ⚙️ How it works
1. Load raw physiological signals from MIMIC III.
2. Apply bandpass filtering (0.5–3 Hz) and noise reduction.
3. Extract time-series features and train Random Forest regression.
4. Evaluate against ANSI/AAMI-style metrics and generate reports.

## 🚀 Getting started
```bash
git clone https://github.com/mukilan2101/ai-enhanced-blood-pressure-monitoring.git
cd ai-enhanced-blood-pressure-monitoring
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python train.py
python evaluate.py
```

## 📈 Results
- Improved CVD prediction from 65% to 78.66%.
- Achieved R² = 0.824 on systolic blood pressure.
- < 5 mmHg error margin on 95% of 2,000+ test cases.

## 📚 What I learned / Next steps
- Designing signal pipelines that remain stable under real clinical noise.
- Managing ML experiment tracking and versioning for medical applications.
- Future: deploy as a real-time monitoring microservice and extend to more datasets.
