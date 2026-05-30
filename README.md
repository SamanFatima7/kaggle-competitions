# Kaggle Competitions

> Starter notebooks, baselines, and competition entries — what I write when the leaderboard opens and there's a fresh dataset to make sense of.

Competition kaggling is its own discipline. The data is usually messy on purpose, the metric is rarely the one you'd pick, and the leaderboard punishes overfitting harder than any textbook. These notebooks are the work-in-progress side of my Kaggle profile — baselines, starter kits, and structured first-pass analyses I share with the community.

---

## 📓 Notebooks in this repo

### 1. Poisonous Mushrooms — Baseline (LB 0.98494) 🍄
Binary classification on a synthetic mushroom-poisonous-or-not dataset. Clean baseline with good cross-validation strategy — a solid starting point that the community forked widely.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/baseline-poisonous-mushrooms)**

---

### 2. CIBMTR — Bridging Gaps in Survival 🩺 (LB 0.679)
A medical survival-analysis competition where the challenge isn't just prediction accuracy but ensuring fairness across patient subgroups. The notebook handles the censored-target setup and the equity-stratified evaluation metric the host required.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/cibmtr-bridging-gaps-in-survival)**

---

### 3. Rohlik Order Forecasting — Simple Guide 📦
A time-series forecasting competition on order volumes. Walks through feature engineering for date features, holiday effects, and lag variables — the standard toolkit for retail forecasting.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/rohlik-order-forcasting-simple-guide)**

---

### 4. WSDM — Get Started (LB 0.619)
A starter notebook for the WSDM 2025 competition. Designed to get a new participant from "I have the data" to "I have a valid submission" in under an hour.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/wsdm-get-started)**

---

### 5. Santa 2024 — Get Started 🎅 (LB 1614.13)
A starter for Kaggle's annual Santa competition, which is always an optimization / combinatorial puzzle rather than standard ML. This one is the route-and-permutation variant.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/santa-2024-get-started)**

---

### 6. Insurance Regression — LB 1.06093
A regression competition with a Poisson-ish target — premium amounts skewed by long-tail outliers. The notebook discusses target transformation, robust loss functions, and ensembling.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/insurance-competition)**

---

### 7. Loan Default — CatBoost Starter Part 2 (LB 0.96977)
A focused CatBoost baseline for a loan-default classification competition. Quick, clean, and tuned with categorical features handled natively. Part 2 of a series.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/loan-catboost-starter-part-2)**

---

### 8. Rainfall Prediction (LB 0.84633) 🌧
A classification competition on rainfall occurrence. Clean baseline with attention to imbalanced classes and time-aware validation.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/rainfall-prediction-lb-0-84633)**

---

### 9. MindMap — Predicting Mental Health 🧠
A classification competition on mental-health outcomes. Handled with sensitivity to the subject matter — the writeup discusses what these models *can't* tell you, alongside what they can.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/mindmap-predicting-mental-health)**

---

### 10. Don't Trust the Leaderboard — A Beginner's Guide ⚠️
Not a competition entry — a guide. Why public-LB rankings often mislead, how to build robust cross-validation that survives the shake-up, and how to read a private-LB drop without blaming the universe. Required reading if you're newer to competitive ML.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/don-t-trust-the-leaderboard-beginner-s-guide)**

---

### 11. Buried Cities Found? 🌿
A starter notebook for the "AI for Archaeology" competition — detecting buried structures from satellite imagery. A nice intersection of CV, geospatial data, and domain knowledge.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/buried-cities-found-ai-says-yes)**

---

### 12. EDA — Useful Insights for Feature Engineering 🧠✨
An EDA notebook scoped specifically at "what features should I engineer next?" — different goal, different structure from a standard EDA. Useful as a template when you're prepping a tabular competition entry.

📔 **[Open on Kaggle →](https://www.kaggle.com/code/samanfatima7/eda-usefull-insights-for-f-e)**

---

## 🛠 Stack

Python · scikit-learn · XGBoost · LightGBM · CatBoost · Optuna · pandas · NumPy

## 📂 How this repo is organized

Each notebook lives in its own `.ipynb` and links to the competition page. Datasets are downloaded automatically by the Kaggle API:

```bash
git clone https://github.com/samanfatima7/kaggle-competitions.git
cd kaggle-competitions
pip install -r requirements.txt
kaggle competitions download -c <competition-name>
jupyter notebook
```

## 🧭 How I approach a new competition

1. **EDA first, model second.** I spend the first session just looking. What does the target look like? What's missing? What's clearly wrong?
2. **Build the dumbest possible baseline.** A LogisticRegression on raw features, a constant predictor — whatever submits in 5 minutes. Now you have something to beat.
3. **Validation strategy before tuning.** A bad CV scheme will burn you on the private LB. Time-series competitions need time-aware splits. Grouped data needs grouped splits. Don't skip this.
4. **Iterate small, log everything.** I keep a simple table: hypothesis → change → CV score → public LB → notes. Most of "winning" is just not losing track.

## 👋 About

Saman Fatima — Kaggle Grandmaster (rank highest 24), data scientist from Pakistan. Profile and full notebook list: [kaggle.com/samanfatima7](https://www.kaggle.com/samanfatima7).

⭐ if any of these helped you — and feel free to fork.
