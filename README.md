# 🌳 Deforestation Detection (Fire Classification)

This project focuses on detecting and classifying fire incidents in India (2021–2023) using **MODIS satellite data**.  
It integrates **Machine Learning**, **Geospatial Analysis**, and **Interactive Visualization** to support deforestation monitoring and disaster response.  

---

## 🚩 Problem Statement  
India faces diverse fire-related incidents such as forest fires, crop residue burning, volcanic activity, and offshore thermal anomalies.  
While MODIS satellites detect fires, **classifying fire types** remains a challenge.  

Accurate classification is critical for:  
- 🚨 Timely disaster response  
- 🌱 Environmental conservation  
- 📊 Agricultural regulation & policymaking  
- 🌍 Climate change research  

---

## 🛠️ Tools & Technologies  
- **Languages**: Python  
- **Libraries**:  
  - NumPy, Pandas – Data processing  
  - Matplotlib, Seaborn – Visualization  
  - Scikit-learn, XGBoost – Modeling  
  - SMOTE – Class balancing  
  - Folium – Interactive maps  
  - Streamlit – Deployment  

- **Data Source**: MODIS (MOD14/MYD14) fire datasets (2021–2023) from [NASA FIRMS](https://firms.modaps.eosdis.nasa.gov/)

---

## 🔎 Methodology  
```python
# 1. Data Collection
# Acquired MODIS fire datasets (2021–2023) from NASA FIRMS

# 2. Preprocessing
# - Removed noise & anomalies
# - Normalized features
# - Filtered water/cloud pixels

# 3. Exploratory Data Analysis
# - Histograms, Boxplots, Pairplots
# - Geospatial fire mapping
# - Temporal fire trends

# 4. Balancing Classes
from imblearn.over_sampling import SMOTE
X_resampled, y_resampled = SMOTE().fit_resample(X, y)

# 5. Model Training
from sklearn.ensemble import RandomForestClassifier
model = RandomForestClassifier()
model.fit(X_train, y_train)

# 6. Evaluation
accuracy = model.score(X_test, y_test)
print("Accuracy:", accuracy)  # Output: 97.76%

# 7. Deployment
# Streamlit app for user-friendly fire classification
