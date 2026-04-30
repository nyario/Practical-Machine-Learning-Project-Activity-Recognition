# Practical-Machine-Learning-Project-Activity-Recognition
## 📌 Project Overview

This project was completed as part of the Coursera *Practical Machine Learning* course.

The goal is to predict the manner in which participants performed barbell lifts using accelerometer data from wearable devices.  
The target variable is **classe**, which represents five different execution styles (A–E), ranging from correct to incorrect exercise form.

---

## 📊 Data

The dataset comes from wearable sensors placed on:
- belt
- forearm
- arm
- dumbbell

Six participants performed barbell lifts in different ways, and sensor data was recorded.

---

## 🧹 Data Processing

The dataset was cleaned using `dplyr`:

- Removed variables with >50% missing values
- Removed non-predictive metadata (timestamps, user info)
- Reduced dimensionality for better model performance

---

## 🤖 Models Used

Two machine learning models were trained:

### 1. Random Forest
- Used as a baseline model
- Strong performance with minimal tuning
- 5-fold cross-validation applied

### 2. Gradient Boosting Machine (GBM)
- More advanced ensemble method
- Sequentially reduces prediction error
- Tuned using cross-validation

---

## 📈 Model Evaluation

| Model           | Accuracy | Out-of-sample Error |
|----------------|----------|---------------------|
| Random Forest   | ~98–99%  | ~1–2%               |
| GBM             | ~99%     | ~1%                 |

GBM slightly outperformed Random Forest and was selected as the final model.

---

## 🎯 Final Prediction

The GBM model was used to predict 20 test cases provided in the assignment.

---

## 🧠 Key Methods

- Data cleaning with `dplyr`
- 5-fold cross-validation (`caret`)
- Ensemble learning (Random Forest + GBM)
- Model comparison using accuracy

---

## 📌 Conclusion

Both models performed very well due to strong signal in sensor data.  
GBM provided slightly better accuracy and was selected as the final model.
