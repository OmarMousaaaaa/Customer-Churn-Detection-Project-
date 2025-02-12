# Customer-Churn-Detection-Project-
This project predicts customer churn, which helps businesses identify customers who are likely to cancel their subscriptions. Retaining existing customers is often more cost-effective than acquiring new ones. The project uses machine learning to analyze customer data and predict churn.

Project Structure

customer-churn-prediction/
├── data/
│   └── Churn_Modelling.csv              # Dataset used for the project
├── notebooks/
│   └── churn_prediction.ipynb           # Jupyter Notebook for the project
├── models/
│   └── customer_churn_model.pkl         # Trained model (Decision Tree)
├── README.md                            # Project documentation
└── requirements.txt                     # Dependencies
Steps to Run the Project
1. Prerequisites
Install Python 3.x.

Install the required libraries by running:

bash
Copy
pip install -r requirements.txt
2. Dataset
The dataset Churn_Modelling.csv is located in the data/ folder.

It contains customer information such as CreditScore, Age, Balance, Geography, and the target variable Exited (1 if the customer churned, 0 otherwise).

3. Running the Code
Open the Jupyter Notebook churn_prediction.ipynb in the notebooks/ folder.

Run the cells step-by-step to:

Load and explore the dataset.

Perform data visualization.

Preprocess the data (encoding, standardization, splitting).

Handle imbalanced data using SMOTE.

Train and evaluate machine learning models (KNN, Naive Bayes, SVM, Decision Tree).

Compare models and save the best one.

4. Trained Model
The best-performing model (Decision Tree) is saved as customer_churn_model.pkl in the models/ folder.

You can load and use the model for predictions:

python
Copy
import joblib
model = joblib.load('models/customer_churn_model.pkl')
predictions = model.predict(X_test)
5. Results
The project compares the performance of four models:

Decision Tree: Best performance with 85% accuracy and 88% ROC-AUC.

KNN, Naive Bayes, and SVM: Results are documented in the notebook.

Key insights:

Features like Age, Balance, and IsActiveMember are important for predicting churn.

SMOTE helped address class imbalance and improved model performance.

Dependencies
The required libraries are listed in requirements.txt:

Copy
pandas
numpy
matplotlib
seaborn
scikit-learn
imbalanced-learn
joblib
jupyter
Install them using:

bash
Copy
pip install -r requirements.txt
How to Contribute
Fork the repository.

Create a new branch for your changes.

Submit a pull request with a detailed description of your updates.
