## 🎯 Problem Statement

Humare paas ek medical dataset hai jisme patients ke health parameters diye gaye hain jaise glucose, blood pressure, BMI, etc.  
Saath hi bataya gaya hai ki unhe diabetes hai ya nahi (0 = nahi, 1 = hai).

**Hamara goal:** Machine Learning ka use karke ek model banana jo naye patients ke data ko dekhkar predict kare ki unko diabetes hai ya nahi.

---

## 📊 Dataset Description

Dataset ka naam hai: **Pima Indians Diabetes Dataset** (Kaggle se liya gaya)

| Column Name                | Matlab (Description)                         |
|----------------------------|----------------------------------------------|
| Pregnancies                | Kitni baar pregnant hui                      |
| Glucose                    | Blood sugar level                            |
| BloodPressure              | Blood pressure (mm Hg)                       |
| SkinThickness              | Triceps ki skin ki motai                    |
| Insulin                    | Insulin level (2 hour baad)                  |
| BMI                        | Body Mass Index (weight/height ratio)       |
| DiabetesPedigreeFunction   | Family history score of diabetes             |
| Age                        | Age in years                                 |
| Outcome                    | 0 = Non-diabetic, 1 = Diabetic               |

---

## ⚙️ Steps Jo Hum Follow Kar Rahe Hain

### 1. Data Cleaning (Safai)
- Kuch columns me 0 values hain, jo actually galat hain (Glucose, BloodPressure, etc.)
- Hum unhe **NaN** maan ke unka **mean** se replace karte hain.

### 2. Feature Scaling
- Sabhi features ko ek hi range me lana (normalization) using `StandardScaler`

### 3. Data Split
- Data ko 2 parts me divide karte hain:
  - **Training (80%)** - jisme model sikhata hai
  - **Testing (20%)** - jisme model ko test karte hain

### 4. Model Training
- Use karte hain: **Random Forest Classifier**
  - Kaafi saare decision trees ka group hota hai
  - Better accuracy aur overfitting se bachav karta hai

### 5. Model Evaluation
- Accuracy nikalte hain
- Precision, Recall, F1-score dekhte hain
- Confusion Matrix banate hain

---

## ✅ Sample Output

Accuracy: ~78%

Classification Report: precision recall f1-score support 0 0.82 0.88 0.85 107 1 0.67 0.56 0.61 47

yaml
Copy
Edit

Confusion matrix bhi plot karte hain visualization ke liye.

---

## 🔚 Summary

- Model 78% accuracy se predict karta hai diabetes.
- Real-life healthcare apps me use ho sakta hai.
- Future me deep learning use karke aur improve kar sakte hain.

---

## 📚 References

- Dataset: https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database
- ML Library: Scikit-learn  
- Visualization: Matplotlib, Seaborn  
- Language: Python
