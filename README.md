# Titanic Survival Prediction 🚢

This project explores the classic **Titanic dataset** to predict passenger survival using a **Decision Tree Classifier** and custom engineered features.

## 📊 Dataset
- Source: Kaggle Titanic Dataset
- Key columns: `pclass`, `sex`, `age`, `sibsp`, `parch`, `fare`, `embarked`, `survived`

## ⚙️ Preprocessing & Feature Engineering
- **Encoding**: `sex` mapped to `0 = male`, `1 = female`
- **New features**:
  - `family_size = sibsp + parch`
  - `is_alone = 1` if `family_size == 0`
  - `sex_class = sex * pclass`
  - `age_class = age * pclass`
- **Dropped columns**: `fare`, `embarked`

## 🧠 Model
- Algorithm: `DecisionTreeClassifier`
- Parameters: `max_depth = 5`
- Train/test split applied for evaluation

## 📈 Results
- **Accuracy**: `82.68%`
- **Average survival probability**: `25.2%`
