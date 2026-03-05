<h1>📈 Hyper-Local Demand Forecasting Engine</h1>

Predictive Inventory Optimization using E-commerce Sales & Cities Weather Proxies
<h2>📌 Business Problem</h2><br>
Quick-commerce platforms (Blinkit, Zepto) lose millions annually due to two critical issues:<br>
Stockouts: Under-predicting demand during rain or festivals leads to lost revenue and customer churn.<br>
High Holding Costs: Over-stocking perishable goods leads to wastage and increased warehouse costs.<br>

<h3>Goal:</h3><br> Build an end-to-end pipeline that predicts SKU-level demand by integrating "Hyper-local" signals (Weather + Holidays) to optimize inventory reorder points.<br>

A machine learning-driven forecasting system designed to predict daily retail revenue with high precision. This project integrates real-time weather data, holiday seasonality, and historical sales trends into a deployed XGBoost pipeline.

<h2>🚀 Project Overview</h2><br>
This project solves the challenge of predicting demand at a "hyper-local" level by accounting for factors that traditional models often miss, such as local weather patterns and regional holidays.<br>

<h2>Key Achievements:</h2><br>
Accuracy: Achieved a WAPE of 8.26% (Weighted Absolute Percentage Error).<br>
Deployment: Fully functional Streamlit Dashboard for real-time "What-If" scenario planning.External Integration: Automated feature engineering using the OpenMeteo API for historical and forecasted weather.<br>

<h2>🛠️ Tech Stack</h2><br>
Language: Python 3.15<br>
ML Frameworks: Scikit-Learn, XGBoostData <br>
Manipulation: Pandas, NumPy<br>
Deployment: Streamlit, Joblib <br>
Environment: Docker (Containerized for scalability)<br>

<h2>📊 Features & Engineering</h2><br>
To achieve high accuracy without data leakage, the model uses the following temporal features: Year, Month, Day, Day of Week, IsWeekend, and Quarter.<br>Weather Signals: Average Temperature and Rainfall Categories (mapped from OpenMeteo).<br>Seasonality & Holidays: Interaction features between holidays and weekends to capture peak demand spikes.<br>Lags & Windows: 7-day and 14-day rolling averages and lag features to capture short-term cyclical trends.<br>

<h2>📈 Model Performance</h2><br>
Initially, the model showed signs of overfitting due to target leakage. By removing post-transaction variables (like Quantity and Customer_Count during initial training) and implementing TimeSeriesSplit cross-validation, the following realistic metrics were achieved:<br>
<h3>MetricValue</h3><br>
WAPE   8.26%<br>
MAE    8,531.61<br>
RMSE   11,056.77<br>
Accuracy~ 91.7%💻 <br>

<h2>Installation & Usage</h2><br>
1. Clone the Repository<br>
2. Bash:git clone https://github.com/yourusername/hyper-local-demand-forecasting.git<br>
cd hyper-local-demand-forecasting<br>
3. Install Dependencies<br>
4. Bash:pip install -r requirements.txt<br>
5. Run the Streamlit App<br>
6. Bash: streamlit run app.py<br>

<h2>🖥️ Dashboard Preview:</h2><br>
The deployed app allows users to enter date and calendar information (Auto-calculates Weekends/Quarters).Weather Forecasts (Temperature/Rainfall).Strategic Variables (Price, Discounts, Expected Quantity) to simulate revenue outcomes.📂 Project StructurePlaintext├── data/               # Training and testing datasets
├── models/             # Saved .joblib files (Preprocessor & Model)<br>
├── notebooks/          # Data Exploration and Model Training scripts<br>
├── app.py              # Streamlit Application<br>
├── requirements.txt    # List of dependencies<br>
└── README.md           # Project documentation<br>


<h3>👨‍💻 Author:</h3><br>
Mithul Krishna Suresh <br>
B.Tech in Computer Science and Engineering <br>
Maulana Azad National Institute of Technology (MANIT), Bhopal<br>

