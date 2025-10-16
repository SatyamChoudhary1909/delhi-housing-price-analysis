# 🏠 House Price Prediction - MagicBricks Dataset

This project builds a **Machine Learning model** to predict house prices based on property features such as area, BHK, bathrooms, parking, furnishing type, and locality.  
The dataset used comes from **MagicBricks** (real-estate listings in India).

---

## ⚙️ Features of the Project
- Cleans and preprocesses the raw housing data  
- Handles missing values and outliers (IQR method)  
- Performs **feature engineering**: `Log_Area`, `Area × BHK`, robust neighborhood encoding  
- Trains and evaluates:
  - **Linear Regression (Scaled)**
  - **Random Forest Regressor (Tuned via GridSearchCV)**
- Provides:
  - Model evaluation metrics (MAE, RMSE, R², Adjusted R²)
  - Feature importance ranking
  - Residual visualization

---

## 📊 Results
| Model | MAE | RMSE | R² | Adjusted R² |
|-------|-----|------|----|-------------|
| Linear Regression | 6.78 L | 13.9 L | 0.7376 | 0.6976 |
| Random Forest | **5.46 L** | **12.48 L** | **0.7898** | **0.7577** |

✅ Random Forest performed best with tuned hyperparameters:
{'bootstrap': False, 'max_depth': 20, 'max_features': 'sqrt','min_samples_leaf': 1, 'min_samples_split': 5, 'n_estimators': 100}

---

## 📈 Sample Prediction
Predicted Price: ₹ 29,55,094
Actual Price: ₹ 32,00,000

---

## 🧠 Key Insights
- Property **Area** and **BHK combination** dominate pricing.
- **Bathrooms** and **Parking availability** have significant effects.
- **Neighborhood** and **Transaction Type** (Resale/New) provide contextual value.

---

## 🚀 Future Improvements
- Add **XGBoost / LightGBM** for better accuracy.  
- Integrate **SHAP** for interpretability.  
- Build a **Streamlit dashboard** for live predictions.

---

## 🧰 Tech Stack
- Python (Pandas, NumPy, Scikit-learn, Matplotlib)
- Jupyter Notebook / Kaggle
- GridSearchCV for hyperparameter tuning

---

## 👨‍💻 Author
**Satyam Choudhary (Zypher)**  
Machine Learning Enthusiast | Robotics & Automation  

---

📌 *This project demonstrates end-to-end ML workflow — from data cleaning to evaluation — on real-world real-estate data.*


