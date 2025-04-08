# Online_retail_data-ML-Predictive-Analysis

## Synthetic Online Retail — ML Prediction Project

This project is an end-to-end Machine Learning pipeline built in **Google Colab** that predicts customer **review scores** based on historical retail transaction data.

---

### 📁 Dataset
- **Source:** `/content/drive/MyDrive/Colab Notebooks/Source Data/synthetic_online_retail_data.csv`
- **Description:** Synthetic dataset representing online retail orders with features like customer demographics, product details, purchase history, and review scores.

---

### 🔍 Objective
Predict the **`review_score`** of a customer order based on attributes like:
- Product details (category, quantity, price)
- Customer demographics (age, gender)
- Order behavior (date of order, city, payment method)

---

### ⚙️ Project Workflow

#### ✅ Step-by-Step Process
1. **Data Loading**
   - Load data from Google Drive into Google Colab.
2. **Data Cleaning**
   - Handle missing values (`review_score`, `gender`, `order_date`)
3. **Feature Engineering**
   - Extract `order_month`, `order_day`, `order_weekday`
   - Create new feature `total_amount = quantity * price`
4. **Target & Features**
   - Target: `review_score`
   - Features: `quantity`, `price`, `total_amount`, `order_month`, `order_weekday`, `age`, `category_id`
5. **Train-Test Split**
6. **Model Training**
   - Algorithm: `RandomForestRegressor`
7. **Model Evaluation**
   - Metrics: R² Score, MAE, MSE, RMSE
8. **Visualization**
   - Scatter plot: Actual vs Predicted review scores
9. **Automation**
   - Pipeline automated to run every **30 minutes** using `schedule`

---

### 📊 Tech Stack
- **Languages:** Python
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn, schedule
- **Environment:** Google Colab + Google Drive

---

### 🕒 Automation
The entire ML pipeline runs every **30 minutes** using the `schedule` library. Each run:
- Loads the latest data
- Cleans & transforms it
- Trains & evaluates the model
- Saves the predictions to a timestamped CSV file in your Drive

---

### 📂 Output
- **Folder:** `/content/drive/MyDrive/Colab Notebooks/Target Files/`
- **Files:** Predicted review scores with timestamped filenames
- **Format:** CSV + PNG visualizations
