# 🌾 Crop Recommendation System  
Data Analysis, Statistical Validation, and Predictive Modeling

## 📌 Project Overview
This project analyzes agricultural data to understand how **environmental conditions** and **soil chemistry** influence crop suitability.  
Using **exploratory data analysis (EDA)**, **statistical testing (ANOVA)**, and **interpretable machine learning models**, the project builds a data-driven foundation for recommending suitable crops under given conditions.

The analysis is designed emphasizing:
- clear problem framing  
- statistical reasoning  
- interpretability  
- real-world agricultural relevance  

## 📘 Notebook Structure & Navigation

This project is implemented in a **well-structured Jupyter Notebook** [Crop_Recommendation_System](crop_recommendation_main.ipynb), designed to guide the reader through the full analytical workflow step by step.  
Readers interested in **detailed code, visualizations, and statistical reasoning** can follow the notebook sections in sequence.

---

## 🎯 Objectives
- Explore relationships between environmental factors, soil chemistry, and crop types  
- Identify statistically significant factors influencing crop growth  
- Compare predictive power of **environmental vs soil-based features**  
- Build interpretable classification models for crop recommendation  

---

## 📊 Dataset Description
The dataset contains crop-specific observations with both **environmental** and **soil nutrient** features.

| Feature | Description |
|-------|------------|
| N | Nitrogen content in soil |
| P | Phosphorus content in soil |
| K | Potassium content in soil |
| temperature | Average temperature (°C) |
| humidity | Relative humidity (%) |
| ph | Soil pH |
| rainfall | Rainfall (mm) |
| label | Crop type |

---

## 🔍 Exploratory Data Analysis (EDA)
The EDA phase focused on understanding feature distributions and relationships.

### Key EDA Steps
- Distribution analysis of temperature, humidity, rainfall, and soil nutrients  
- Correlation heatmap to identify feature interdependencies  
- Crop-wise nutrient distribution analysis  
- Pairwise environmental relationship plots grouped by crop categories:
  - Beverage crops  
  - Fiber crops  
  - Fruits  
  - Cereals  
  - Legumes & pulses  

### Key EDA Insights
- Most environmental variables are weakly correlated, indicating **independent predictive value**  
- Phosphorus (P) and Potassium (K) show moderate correlation (r ≈ 0.74)  
- Clear environmental separation exists between:
  - humid vs dryland crops  
  - rainfed vs low-rainfall crops  

---

## 🧮 Statistical Analysis (ANOVA)
One-way ANOVA tests were conducted to examine whether environmental factors differ significantly across crop types.

### ANOVA Results Summary

| Factor | F-statistic | p-value |
|------|------------|---------|
| Temperature | 102.18 | < 0.001 |
| Humidity | 3103.71 | < 0.001 |
| Rainfall | 605.53 | < 0.001 |

### Interpretation
All three environmental factors show **statistically significant differences across crops**, confirming their relevance for predictive modeling.  
Humidity emerged as the most discriminative variable.

---

## 🤖 Predictive Modeling Approach

### Models Built
Three interpretable Decision Tree models were trained:

| Model | Features Used | Accuracy |
|-----|--------------|---------|
| Environmental Model | Temperature, Humidity, Rainfall | **0.91** |
| Soil Chemistry Model (All) | N, P, K, pH | **0.78** |
| Soil Chemistry Model (Reduced) | N, P, pH | **0.58** |

### Key Modeling Insights
- Environmental factors alone provide **strong predictive power**  
- Soil chemistry alone still performs well, confirming nutrient importance  
- Removing Potassium caused a **20% accuracy drop**, showing that:
  > correlation does not imply redundancy  

---

## 📊 Model Evaluation
- Classification reports and confusion matrices show **strong diagonal dominance**, indicating reliable predictions  
- Some crops (e.g., orange, pomegranate) exhibit mild confusion due to overlapping environmental ranges  
- Feature importance analysis aligns with ANOVA findings  

---

## ⚖️ Comparative Analysis
- **Environmental conditions** determine broad crop suitability  
- **Soil chemistry** refines local-level recommendations  
- The two domains are **complementary**, not interchangeable  

---

## ✅ Conclusion
- Environmental variables (temperature, humidity, rainfall) are the primary drivers of crop differentiation  
- Soil nutrients, especially P and K, provide essential secondary information  
- Decision Trees offer strong performance while maintaining interpretability  
- Statistical validation (ANOVA) strengthened feature selection and model credibility  

This project demonstrates how **data analysis + statistics + machine learning** can be combined to create an explainable and practical crop recommendation system.

---

## 💡 Lessons Learned
- Statistical testing improves confidence in feature selection  
- Correlated variables can still provide unique predictive value  
- Interpretability is crucial in domain-driven problems like agriculture  
- Visual EDA is essential for understanding complex environmental interactions  

---

## 🚀 Future Work
- Train ensemble models (Random Forest, XGBoost) for improved generalization  
- Combine environmental and soil features into a hybrid production model  
  
---

## 🛠️ Tech Stack
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- SciPy  

---

