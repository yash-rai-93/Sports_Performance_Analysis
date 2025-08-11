# 🏸 Sports Performance Analysis – Intramural Badminton Tournament

## 📌 Overview
This project analyzes **intramural badminton match data** to uncover factors that most strongly influence **match outcomes**.  
Using **Logistic Regression** and **Principal Component Analysis (PCA)**, we model performance, identify winning indicators, and visualize underlying performance dimensions.

---

## 🎯 Objectives
- Gather match data (scores, playing time, position).
- Engineer richer features like `Points Scored`, `Opponent Points Scored`, `Point Difference`.
- Analyze correlations and distributions of performance metrics.
- Predict win probability using Logistic Regression.
- Visualize performance dimensions using PCA.

---

## 📂 Project Structure
Sports_Performance_Analysis/
│
├── images/ # Plots for README
│ ├── pca_plot.png
│ ├── correlation_heatmap.png
│ ├── regression_coefficients.png
│
├── Updated_Badminton_Tournament_Data.xlsx # Dataset
├── MDSprojSports_Tanishk.ipynb # Full analysis
├── README.md # Documentation
└── .gitignore # Ignore unnecessary files

---

## 📊 Key Insights

### Correlation Heatmap
<img width="932" height="835" alt="image" src="https://github.com/user-attachments/assets/e9976699-5271-454d-8391-0fa765f83346" />
 
- **Point Difference** has the strongest positive correlation with winning (`+0.90`).
- **Rallies Won** is also highly correlated with winning (`+0.70`).
- **Opponent Points Scored** has a strong negative correlation (`-0.69`).
- **Fouls Made** has a smaller but still negative correlation (`-0.26`).

---- Exploratory Data Analysis (EDA) & Visualization ---
<img width="1483" height="984" alt="image" src="https://github.com/user-attachments/assets/4ab90bf1-4bef-4b93-b3d7-fde499fdd916" />

<img width="1784" height="584" alt="image" src="https://github.com/user-attachments/assets/c83d3880-705d-4e1f-a5bf-1c4510559f8e" />

### Logistic Regression – Feature Impact
- **Top positive factors:**
  - `Point Difference` (Odds Ratio ~ 6.1)
  - `Rallies Won` (Odds Ratio ~ 2.4)
- **Negative factors:**
  - `Fouls Made` (Odds Ratio ~ 0.72)
  - `Number of Games` (Odds Ratio ~ 0.9)
- Model accuracy: **95.3%**

---

### PCA Visualization
<img width="691" height="550" alt="image" src="https://github.com/user-attachments/assets/fc14038a-1889-4a17-b358-8c5f89987e8a" />
  
- **PC1 (50.3% variance):** Match intensity & duration.
- **PC2 (23.4% variance):** Match dominance.
- Win/Loss separation happens mainly along **PC2**, indicating dominance is a strong driver of outcomes.

---

## 🛠 Methods Used
- **Feature Engineering:** Derived key performance metrics from raw scores.
- **Exploratory Data Analysis (EDA):** Distribution plots, boxplots, scatter plots, correlation heatmaps.
- **Modeling:** Logistic Regression for win probability prediction.
- **Dimensionality Reduction:** PCA for performance dimension visualization.

---
