Free2Move EV Rental Dataset — Technical Analysis
A data analysis project exploring electric vehicle rental patterns using the Free2Move dataset. The notebook investigates battery usage behavior, customer rental habits, and vehicle performance across 51 unique EVs.

📌 Project Overview
This notebook performs a structured exploratory data analysis (EDA) on a shared Free2Move EV rental dataset. The analysis separates customer rentals from service/agent activity and investigates the factors influencing battery consumption, charging behavior, and vehicle utilization.

🔍 Analysis Breakdown
The notebook is organized into 10 mini-tests, each targeting a specific hypothesis or question:
#TestKey Finding1Rental Duration vs Battery UsedLow correlation — usage time is a poor predictor of charge consumed2Starting Charge vs Battery UsedVehicles below 20% charge are rarely rented; most trips use under 20% battery3Charge Start Level DistributionHigher charge levels (80–100%) see significantly higher rental probability4Vehicle Utilization FrequencyOne vehicle (dc753ee...) shows abnormally low rental frequency5End Charge Level — Customer vs ServiceService agents are most active when charge is below 20% or above 90%6Charging During RentalsMajority of customers do not charge the vehicle during rental7Duration vs Charging BehaviorLonger rentals correlate with a higher likelihood of in-rental charging8Start Charge vs Charging BehaviorCustomers are more likely to charge when the starting battery is below 30%9Duration × Start Charge MatrixA diagonal preference boundary emerges — high charge preferred even for short trips10Per-Vehicle PerformanceOne vehicle (1c347a2f...) is repeatedly rented at low charge levels

🛠️ Tech Stack

Python 3
pandas — data manipulation and feature engineering
matplotlib — visualizations (scatter plots, histograms, bar charts)
numpy — numerical operations
scikit-learn — linear regression (imported for potential modelling)


📁 Dataset
The dataset (Free2Move.csv) contains EV rental records with the following key fields:
ColumnDescriptionSTARTED_TIMERental start timestampFINISHED_TIMERental end timestampCHARGELEVELSTARTBattery percentage at start of rentalCHARGELEVELENDBattery percentage at end of rentalCHARGEDWhether the vehicle was charged during rentalSERVICERENTALWhether the trip was made by a service agentVEHICLE_IDUnique vehicle identifier

Note: The dataset is not included in this repository. To run the notebook, place Free2Move.csv in the same directory and update the file path in Cell 4.


🚀 Getting Started

Clone the repository

bash   git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
   cd YOUR_REPO

Install dependencies

bash   pip install pandas matplotlib numpy scikit-learn jupyter

Add the dataset
Place Free2Move.csv in the project root and update the path in the notebook:

python   data = pd.read_csv('Free2Move.csv')  # update from the original hardcoded path

Launch the notebook

bash   jupyter notebook Free2Move_assessment.ipynb

📊 Key Insights

Customers strongly prefer renting vehicles with higher battery levels, regardless of intended trip duration.
Battery consumption has little correlation with rental duration — other factors dominate.
Service agents play a critical role in recharging vehicles below 20%, acting as the primary buffer for low-battery states.
A small number of vehicles show consistently underperforming charge patterns, which may warrant operational attention.


📄 License
This project was completed as a technical assessment. Dataset rights belong to Free2Move.
