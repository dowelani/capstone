# 🧠 Stroke Prediction Project

---

## **Overview**
This project focuses on predicting stroke occurrences based on health and demographic factors using machine learning models.  
The main goal was to identify the best model to minimize false negatives (missed stroke cases), which is crucial in healthcare applications.

---

## **Dataset**
- Source: [Kaggle - Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
- Features include: gender, age, hypertension, heart disease, marital status, work type, residence type, average glucose level, BMI, smoking status.
- Target variable: **stroke** (binary classification: 0 = No Stroke, 1 = Stroke)

---

## **Preprocessing**
- Removed unnecessary features: **id** column (unique identifier).
- Handled class imbalance using **SMOTE** (Synthetic Minority Over-sampling Technique).
- Split data into **training** and **test sets**.

---

## **Exploratory Data Analysis (EDA) Highlights**
- **Age** distribution showed most individuals between **50–54 years**.
- **Average glucose level** was **right-skewed**, most counts between **80–85**.
- **BMI** appeared **normally distributed**, with the peak between **26–28**.
- **Binary features** (hypertension, heart disease, stroke) showed far more people without these conditions.
- Most numerical features had **positive but weak correlations** (generally < 0.2).
- **Violin plots** revealed:
  - More strokes occur after **age 40**.
  - Strokes were frequent with glucose levels between **50 and 100**.
  - Strokes mostly occurred with BMI between **20 and 35**.

---

## **Modeling and Evaluation**
Evaluated the following models:
- Logistic Regression
- Decision Tree
- Random Forest
- K-Nearest Neighbors (KNN)

### **Key Test Set Results**

| Model                | Accuracy | Precision | Recall | F1 Score |
|----------------------|:--------:|:---------:|:------:|:--------:|
| Random Forest         | 0.922466 | 0.894077  | 0.958486| 0.925162 |
| Decision Tree         | 0.864469 | 0.835017  | 0.908425| 0.870175 |
| Logistic Regression   | 0.841270 | 0.825378  | 0.865690| 0.845054 |
| KNN                   | 0.889499 | 0.832985  | 0.974359| 0.898143 |

---

## **Final Model**
- **Selected Model**: 🏆 **Random Forest Classifier**

### **Reason for Selection:**
- Achieved the **highest performance** across all key metrics.
- Particularly strong **Recall (95.8%)**, crucial for identifying stroke cases.
- **Robust** against overfitting.
- Handles **class imbalance** well (especially post-SMOTE).
- Capable of capturing **complex feature interactions**.

### **Configuration of Final Model:**
- `n_estimators`: 100
- `max_depth`: 'None'
- Other parameters kept at default settings.

---

## **Conclusion and Future Work**
### **Summary:**
- Random Forest outperformed other models, making it the best fit for stroke prediction.
- High Recall is crucial in medical diagnosis tasks like this to avoid missing true stroke cases.

### **Limitations:**
- Dataset size was relatively small for medical predictions.
- Certain important health features (e.g., family history, blood pressure readings) were missing.

### **Future Directions:**
- Incorporate additional relevant features (e.g., blood pressure, cholesterol levels).
- Test ensemble methods or stacking for even better performance.
- Explore deep learning approaches for further improvement.

---

## **References**
- [Stroke Prediction Dataset - Kaggle](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Imbalanced-learn (SMOTE) Documentation](https://imbalanced-learn.org/stable/)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [NumPy Documentation](https://numpy.org/doc/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Seaborn Documentation](https://seaborn.pydata.org/)

---

# 🚀 Thank you!

