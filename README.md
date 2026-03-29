# 🚗 Free2Move EV Rental Dataset — Technical Analysis

A data analysis project exploring electric vehicle rental patterns using the Free2Move dataset. The notebook investigates battery usage behavior, customer rental habits, and vehicle performance across 51 unique EVs.

---

## 📓 Notebook

[![Open in nbviewer](https://img.shields.io/badge/View-nbviewer-orange?logo=jupyter)](https://nbviewer.org/github/YOUR_USERNAME/YOUR_REPO/blob/main/Free2Move_assessment.ipynb)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_USERNAME/YOUR_REPO/blob/main/Free2Move_assessment.ipynb)

> Replace `YOUR_USERNAME` and `YOUR_REPO` with your actual GitHub details.

---

## 📌 Project Overview

This notebook performs a structured exploratory data analysis (EDA) on a shared Free2Move EV rental dataset. The analysis separates customer rentals from service/agent activity and investigates the factors influencing battery consumption, charging behavior, and vehicle utilization.

---

## 🔍 Analysis Breakdown

The notebook is organized into 10 mini-tests, each targeting a specific hypothesis or question:

| # | Test | Key Finding |
|---|------|-------------|
| 1 | Rental Duration vs Battery Used | Low correlation — usage time is a poor predictor of charge consumed |
| 2 | Starting Charge vs Battery Used | Vehicles below 20% charge are rarely rented; most trips use under 20% battery |
| 3 | Charge Start Level Distribution | Higher charge levels (80–100%) see significantly higher rental probability |
| 4 | Vehicle Utilization Frequency | One vehicle (`dc753ee...`) shows abnormally low rental frequency |
| 5 | End Charge Level — Customer vs Service | Service agents are most active when charge is below 20% or above 90% |
| 6 | Charging During Rentals | Majority of customers do not charge the vehicle during rental |
| 7 | Duration vs Charging Behavior | Longer rentals correlate with a higher likelihood of in-rental charging |
| 8 | Start Charge vs Charging Behavior | Customers are more likely to charge when the starting battery is below 30% |
| 9 | Duration × Start Charge Matrix | A diagonal preference boundary emerges — high charge preferred even for short trips |
| 10 | Per-Vehicle Performance | One vehicle (`1c347a2f...`) is repeatedly rented at low charge levels |

---

## 🛠️ Tech Stack

- **Python 3**
- `pandas` — data manipulation and feature engineering
- `matplotlib` — visualizations (scatter plots, histograms, bar charts)
- `numpy` — numerical operations
- `scikit-learn` — linear regression (imported for potential modelling)

---

## 📁 Dataset

The dataset (`Free2Move.csv`) contains EV rental records with the following key fields:

| Column | Description |
|--------|-------------|
| `STARTED_TIME` | Rental start timestamp |
| `FINISHED_TIME` | Rental end timestamp |
| `CHARGELEVELSTART` | Battery percentage at start of rental |
| `CHARGELEVELEND` | Battery percentage at end of rental |
| `CHARGED` | Whether the vehicle was charged during rental |
| `SERVICERENTAL` | Whether the trip was made by a service agent |
| `VEHICLE_ID` | Unique vehicle identifier |

> **Note:** The dataset is not included in this repository. To run the notebook, place `Free2Move.csv` in the same directory and update the file path in Cell 4.

---

## 🚀 Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
   cd YOUR_REPO
   ```

2. **Install dependencies**
   ```bash
   pip install pandas matplotlib numpy scikit-learn jupyter
   ```

3. **Add the dataset**  
   Place `Free2Move.csv` in the project root and update the path in the notebook:
   ```python
   data = pd.read_csv('Free2Move.csv')  # update from the original hardcoded path
   ```

4. **Launch the notebook**
   ```bash
   jupyter notebook Free2Move_assessment.ipynb
   ```

---

## 📊 Key Insights

- Customers strongly prefer renting vehicles with **higher battery levels**, regardless of intended trip duration.
- **Battery consumption has little correlation with rental duration** — other factors dominate.
- Service agents play a critical role in **recharging vehicles below 20%**, acting as the primary buffer for low-battery states.
- A small number of vehicles show **consistently underperforming charge patterns**, which may warrant operational attention.

---

## 📄 License

This project was completed as a technical assessment. Dataset rights belong to Free2Move.
