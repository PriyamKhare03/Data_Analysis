📊 Logistic Regression for Bank Marketing Prediction

🧠 Project Overview

This project builds a Logistic Regression classification model to predict whether a customer will subscribe to a bank term deposit based on marketing campaign data.

The project follows a complete Data Science workflow:

Data Understanding → EDA → Preprocessing → Handling Imbalance → Model Training → Evaluation

This demonstrates practical experience with:

- Large real-world dataset (45K+ records)
- Feature engineering and encoding
- Class imbalance handling
- Model training using PyTorch
- Performance analysis

---

🎯 Problem Statement

Banks conduct marketing campaigns to promote term deposits.
The goal of this project is to predict:

Will a customer subscribe?

Target variable:

- 1 → Yes
- 0 → No

This helps businesses:

- Target potential customers
- Improve campaign efficiency
- Reduce marketing costs

---

📁 Dataset Information

- Total Records: 45,211
- Features: 17 original variables
- Types:
  - Numerical (age, balance, duration, etc.)
  - Categorical (job, marital, education, etc.)

Key Observations

- No missing values
- Presence of outliers
- Class imbalance:
  - No: 39,922
  - Yes: 5,289

---

🔍 Exploratory Data Analysis (EDA)

1. Target Variable Distribution

![](images/download.png)

Insight

- Dataset is highly imbalanced
- Majority customers did not subscribe
- Imbalance handling is required

---

2. Target Distribution (Alternative Visualization)

![](images/download_1.png)

Insight

- Confirms class imbalance visually
- Helps understand the proportion of each class

---

3. Numerical Features Boxplot

![](images/download_2.png)

Insight

- Shows distribution of numerical features
- Indicates presence of outliers
- Highlights the need for feature scaling

---

⚙️ Data Preprocessing

Steps performed:

1. Converted target variable:

yes → 1
no → 0

2. One-Hot Encoding

- Applied using "pd.get_dummies()"

3. Feature Scaling

- Used StandardScaler for numerical columns

4. Train-Test Split

- 80% Training
- 20% Testing

---

⚖️ Handling Class Imbalance

Applied Random Oversampling on training data.

Before Resampling

- Class 0: 31,970
- Class 1: 4,198

After Resampling

- Class 0: 31,970
- Class 1: 31,970

This ensures the model learns equally from both classes.

---

🤖 Model Training

Logistic Regression implemented using PyTorch:

- Model: Linear Layer
- Activation: Sigmoid
- Loss Function: Binary Cross Entropy (BCELoss)
- Optimizer: Adam
- Epochs: 1500

---

4. Training Loss Trend

![](images/download_3.png)

Insight

- Loss decreases and stabilizes
- Indicates successful learning and convergence

---

📈 Model Performance

Accuracy: 84.25%

Confusion Matrix Results:

- True Negative: 6711
- False Positive: 1241
- False Negative: 183
- True Positive: 908

Classification Report Summary

Class| Precision| Recall| F1-score
No (0)| 0.97| 0.84| 0.90
Yes (1)| 0.42| 0.83| 0.56

Insight

- High recall for positive class
- Model is effective in identifying potential subscribers

---

🧱 Project Structure

02_Logistic_Regression/
│
├── Logistic_Regression.ipynb
├── bank-full.csv
├── images/
│   ├── download.png
│   ├── download_1.png
│   ├── download_2.png
│   └── download_3.png
└── README.md

---

🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- PyTorch

---

📚 Key Learnings

- Working with large real-world datasets
- Handling class imbalance using oversampling
- Feature encoding and scaling
- Implementing Logistic Regression using PyTorch
- Evaluating classification performance
- Understanding business impact of model results

---

🏁 Conclusion

The Logistic Regression model achieved 84% accuracy and successfully identified potential customers likely to subscribe to term deposits. By addressing class imbalance and applying proper preprocessing, the model provides meaningful insights for targeted marketing strategies.

---

👨‍💻 Author

Priyam Khare
MCA | Data Analytics | Machine Learning | Python | SQL
