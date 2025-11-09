# 🦁 Zoo Animal Classification using Random Forest

## 📘 Project Overview
This project aims to classify animals into different categories based on their biological and behavioral characteristics.  
The dataset used contains features such as whether the animal has hair, feathers, lays eggs, breathes, is aquatic, etc.  
A **Random Forest Classifier** model was trained to predict the **class type** of an animal with very high accuracy.

---

## 📊 Dataset
**Source:** [Zoo Animal Classification Dataset (Kaggle)](https://www.kaggle.com/datasets/uciml/zoo-animal-classification)  

- `zoo.csv` — contains animal features  
- `class.csv` — contains class descriptions  

**Features Example:**
| Feature | Description |
|----------|--------------|
| hair | Has hair (1 = yes, 0 = no) |
| feathers | Has feathers |
| eggs | Lays eggs |
| milk | Produces milk |
| aquatic | Lives in water |
| airborne | Can fly |
| legs | Number of legs |
| class_type | Animal category (1–7) |

---

## ⚙️ Technologies Used
- Python 3  
- pandas, numpy  
- matplotlib, seaborn  
- scikit-learn (RandomForestClassifier)  

---

## 🧠 Model Training
- Split data into training (80%) and testing (20%) sets  
- Used **RandomForestClassifier** with `class_weight='balanced'` to handle uneven classes  
- Achieved **100% accuracy** on the test set  

```python
model = RandomForestClassifier(n_estimators=100, random_state=42, class_weight='balanced')
model.fit(X_train, y_train)
