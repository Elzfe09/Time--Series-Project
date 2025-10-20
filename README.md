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
Compute rolling **mean**, **sum**, or **standard deviation** over a fixed pass time window (e.g., 7 days) to reveal **moving trends**, **seasonality**, or **short-term patterns** in the rental count and make a series stationery.

### 🔺 3. Differencing  
Calculate the **change between current and n previous values** to make the series stationary and remove long-term trends — helping models detect fluctuations more effectively.

---

## 🚀 Outcome  

By applying these transformations, we can:
- 📊 Expose underlying trends  
- 🧠 Improve model interpretability  
- ⚡ Boost forecasting accuracy  

---


# ✈️ Time Series Forecasting on Air Passenger Data (ARIMA Model)

> 🧠 Predicting airline passenger trends to empower smarter decisions in the aviation industry.  

Airline demand is **highly dynamic** — passenger volume can change rapidly due to seasonal patterns, events, or external shocks.  
Accurate **forecasting** helps stakeholders make better decisions on:
- 🛫 Aircraft deployment on specific routes  
- ⛽ Fuel cost estimation  
- 💰 Revenue projection per route  
- 🧩 Anticipating unforeseen circumstances (e.g., pandemics or market shifts)

---

## 🗂️ About the Dataset  

This dataset represents **airport traffic trends** as a **percentage of the baseline** traffic volume during  
📅 **Baseline Period: 1st February – 15th March 2020**  

Each value shows how airport activity compares to pre-pandemic norms — allowing us to track recovery or decline trends in global air travel.  

---

## ⚙️ Working Structure  

| Step | Description |
|------|--------------|
| 1️⃣ | **Import necessary libraries** (`pandas`, `numpy`, `matplotlib`, `statsmodels`, etc.) |
| 2️⃣ | **Load dataset** and set `date` as index for time series formatting |
| 3️⃣ | **Perform data overview** – shape, types, missing values |
| 4️⃣ | **Remove unimportant features** to focus on traffic trends |
| 5️⃣ | **EDA (Exploratory Data Analysis)** – identify trends, patterns, and anomalies |
| 6️⃣ | **Visualize** traffic over time for specific regions or countries 📈 |

---

## 🧪 Technique Overview  

### 🧭 1. Dickey-Fuller Test  
A statistical test to check whether the series is **stationary**.  
- If **p-value < 0.05** → Data is **stationary** ✅  
- If **p-value > 0.05** → Data is **non-stationary** ❌  

### 🧮 2. KPSS Test  
A complementary test — works **opposite** of Dickey-Fuller.  
- If **p-value < 0.05** → Data is **non-stationary**  
- If **p-value > 0.05** → Data is **stationary**

### 🔁 3. Differencing  
Used to **remove trend** and make data stationary by subtracting each value from its previous one:
\[
Y'_t = Y_t - Y_{t-1}
\]
This reveals **pure fluctuations** without long-term growth bias.

### 🔗 4. Autocorrelation (ACF)  
Shows **how strongly** today’s passenger count relates to values from previous time steps (lags).  
> 🔍 Used to detect repeating patterns or seasonality.

### 🧩 5. ARIMA Model  
ARIMA combines three components:
- **AR (AutoRegressive)** → relationship with past values  
- **I (Integrated)** → differencing for stationarity  
- **MA (Moving Average)** → relationship with past forecast errors  

ARIMA helps forecast future passenger volumes based on learned temporal dynamics.  

---

## 🛠️ Tech Stack  

| Tool | Description |
|------|--------------|
| 🐍 **Python** | Main programming language |
| 📦 **Pandas / NumPy** | Data manipulation |
| 🧮 **Scikit-learn / Statsmodels** | Feature creation & model evaluation |

---
