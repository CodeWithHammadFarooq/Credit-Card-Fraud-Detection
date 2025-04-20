💼 Project Title: Credit Card Fraud Detection using Logistic Regression
🎯 1. Objective
"The goal of this project was to detect fraudulent transactions using machine learning. Since fraud cases are rare, the dataset was highly imbalanced, and I applied techniques like under-sampling to address this."

📂 2. Dataset
Used the Credit Card Fraud Detection dataset with ~284,807 transactions.

Each row is a transaction, and the Class column indicates:

0 = Legitimate Transaction

1 = Fraudulent Transaction

Most features are PCA-transformed for anonymity.

🧹 3. Data Preprocessing
Checked for null values — none found.

Explored class distribution:

Legitimate transactions: ~284,315

Fraudulent transactions: ~492

"This confirmed that the dataset is highly imbalanced, which can mislead the model."

⚖️ 4. Under-Sampling
"To balance the dataset, I randomly sampled 492 legitimate transactions to match the 492 fraudulent ones."

Created a balanced dataset by combining:

492 legit transactions

492 fraudulent transactions

🧪 5. Feature & Target Separation
Dropped the Class column to get feature set X

Used the Class column as target variable Y

🔀 6. Train-Test Split
"I split the data into 80% training and 20% testing sets using train_test_split() and kept the class distribution intact using stratify=Y."

🧠 7. Model Training
Used Logistic Regression, a simple yet effective classification algorithm.

Trained the model on the balanced training data.

✅ 8. Model Evaluation
Evaluated the model using accuracy score:

python
Copy
Edit
Accuracy on Training Data: ~93.1%
Accuracy on Test Data: ~91.3%
"Although accuracy was good, I understand that for imbalanced datasets, metrics like precision, recall, and F1-score are also critical — which can be further implemented."

⚙️ 9. Tools & Libraries
Pandas, NumPy for data manipulation

Scikit-learn for model training and evaluation

Jupyter Notebook for development

🔍 10. Real-World Use Case
"This model can be integrated into a financial institution’s transaction system to flag suspicious activities for further investigation, thus reducing fraud losses."

💡 Optional Improvements
You can mention things you plan to add:

Try SMOTE (Synthetic Minority Over-sampling Technique) for better sampling.

Try other models: Random Forest, XGBoost.

Use confusion matrix, ROC curve, precision/recall scores.
