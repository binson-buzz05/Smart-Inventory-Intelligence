# Smart-Inventory-Intelligence
An end-to-end machine learning system for retail operations, covering demand forecasting, inventory risk monitoring, and pricing optimization — built with Python, scikit-learn, and Streamlit.

Overview

Retailers lose revenue in three predictable ways: understocking high-demand products, overstocking slow movers, and mispricing against competitors. This project tackles all three with a unified data pipeline and an interactive dashboard for exploring predictions in real time.

Features
Demand Forecasting — predicts sales quantity using price, promotions, seasonality, and customer segment data (Random Forest, tuned via GridSearchCV)
Inventory Risk Monitoring — classifies products as stockout-risk vs. healthy stock, plus ABC inventory segmentation by value contribution
Pricing Optimization — models sales volume sensitivity to price and recommends raise / lower / maintain actions based on elasticity and competitor gap
Interactive Dashboard — Streamlit app to explore data, run live predictions, and visualize trends
Tech Stack

Python · pandas · NumPy · scikit-learn · Streamlit · Matplotlib / Seaborn · Jupyter Notebook

Project Structure
Smart_Inventory_Intelligence/
├── data/                 # Raw CSV datasets
├── notebooks/            # EDA, model training, and evaluation notebook
├── models/               # Saved trained models (.pkl)
├── outputs/              # Generated charts and result CSVs
├── app.py                # Streamlit dashboard
├── requirements.txt
└── README.md
Models & Results
Task	Model	Metric
Demand Forecasting	Random Forest (tuned)	R², MAE reported in notebook
Stockout Risk	Random Forest Classifier	Accuracy, precision/recall
Pricing / Sales Volume	Gradient Boosting Regressor	R², MAE reported in notebook

Model comparison across Linear Regression, Random Forest, and Gradient Boosting is included in the notebook, along with 5-fold cross-validation and hyperparameter tuning.

How to Run

1. Clone the repo

bash
git clone https://github.com/yourusername/Smart-Inventory-Intelligence.git
cd Smart-Inventory-Intelligence

2. Install dependencies

bash
pip install -r requirements.txt

3. Train the models Run all cells in notebooks/ — this generates the .pkl model files and output charts.

4. Launch the dashboard

bash
streamlit run app.py

Opens at http://localhost:8501.

Dashboard Preview

<img width="1313" height="643" alt="image" src="https://github.com/user-attachments/assets/ca1db6b3-24d1-4a13-9bef-5ffacb110076" />


Future Improvements
Deploy live on Streamlit Community Cloud
Add time-series models (e.g. Prophet, ARIMA) for demand forecasting comparison
Automate retraining pipeline on new data
Author

Built by Binson Bajracharya — LinkedIn [· Portfolio] (https://www.linkedin.com/in/binson-bajracharya-79536a3b9/)
