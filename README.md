# ⚡ Time-Series Feature Engineering for Predictive Analysis  

> 🚴‍♀️ Exploring the power of **time-based insights** to improve predictive model performance.  

This repository contains **two major initiatives** under the **Time Series Modeling** framework — focused on uncovering meaningful temporal patterns through **feature engineering** and smart data preprocessing.  

---

## 🧩 1️⃣ Task 1: Feature Engineering (Data Preprocessing)

🎯 The goal is to **transform raw data** to highlight hidden trends and boost model accuracy by applying various **feature engineering** techniques on the **Bike Sharing Dataset**.

---

## 📊 About the Dataset  

The **Bike Sharing Dataset** records **daily and hourly rental counts** for a public bicycle system, influenced by external factors (all in numerical, standardize, label encode, dummy values) such as:
- 📅 **Date and time**
- 🌡️ **temperature**
- 💧 **Humidity**
- 🌬️ **Windspeed**
- 🏖️ **Holiday**
- 🧑‍💼 **Working day**
- and more

These attributes help analyze how environmental and social conditions affect bicycle rental behavior over time.

---

## ⚙️ Feature Engineering Steps  

> 🕒 Before anything else: **set the date as the index** for proper time-series structure.

### 🔁 1. Shift  
Create lagged versions of the series (e.g., `cnt(t-1)`, `cnt(t-2)`...) to capture temporal dependencies and delayed effects.

### 📈 2. Rolling Statistics  
Compute rolling **mean**, **sum**, or **standard deviation** over a fixed pass time window (e.g., 7 days) to reveal **moving trends**, **seasonality**, or **short-term patterns** in the rental count.

### 🔺 3. Differencing  
Calculate the **change between current and n previous values** to make the series stationary and remove long-term trends — helping models detect fluctuations more effectively.

---

## 🚀 Outcome  

By applying these transformations, we can:
- 📊 Expose underlying trends  
- 🧠 Improve model interpretability  
- ⚡ Boost forecasting accuracy  

---

## 🛠️ Tech Stack  

| Tool | Description |
|------|--------------|
| 🐍 **Python** | Main programming language |
| 📦 **Pandas / NumPy** | Data manipulation |
| 🧮 **Scikit-learn / Statsmodels** | Feature creation & model evaluation |

---

## Task 2: Time Series Forecasting using


