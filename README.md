
  
# AAI-530-04-Final-Project-Code-Team-4
This project is part of the **Data Analytics and Internet of Things** (AAI-530-01) course in the Applied Artificial Intelligence Program at the University of San Diego (USD).

**-- Project Status: [completed]**

### Installation

To run this project on your local machine:

1. Clone the repository:
   ```bash [url]
   git clone https://github.com/apadin-usd/AAI-530-04-Final-Project-Group-4.git```
2. Run with Jypiter: https://jupyter.org/install 

## Project Intro/Objective
This project aims to develop a set of predictive model for monitoring and optimizing water quality in freshwater aquaponics systems dedicated to catfish farming. By leveraging IoT sensor data and machine learning techniques, we analyze key environmental and biological factors influencing water health and fish well-being. Our system integrates real-time data collection from twelve aquaponics ponds, each monitored by an ESP-32 microcontroller equipped with sensors measuring parameters such as turbidity, temperature, ammonia, nitrate, dissolved oxygen, and pH.

### Contributors
- Alexander J Padin
- Kevin Pooler
- Manikandan Perumal

### Methods Used
- Exploratory Data Analysis (EDA)
- Linear Regression
- LSTM

### Technologies
- Python
- Jupyter Notebook

## Project Description

#### Dataset
- **Source**: https://www.kaggle.com/datasets/ogbuokiriblessing/sensor-based-aquaponics-fish-pond-datasets
- **Variables**: 
	- Date/Time: Timestamp of the recorded data.
	- Temperature: Water temperature in degrees Celsius.
	- Turbidity: Cloudiness or haziness of the water due to suspended particles.
	- Dissolved Oxygen (DO): Oxygen available in water, essential for fish respiration and aerobic microbial processes.
	- pH: Acidity or alkalinity of the water, crucial for maintaining optimal conditions.
	- Ammonia: Concentration of ammonia, a byproduct of fish waste and organic matter decomposition.
	- Nitrate: End-product of the nitrification process, impacting plant and microbial interactions.
	- Fish Population: Number of fish in the pond at the time of measurement.
	- Fish Length: Length of individual fish, indicating growth trends.
	- Fish Weight: Mass of individual fish, reflecting health and development.
	- Size: The dataset contains [rows] rows and [column] columns.

#### Models Used
- **Traditional ML**: Linear Regression to predict Nitrate
- **Deep Learning ML**: LSTM to predict pH

#### Project Steps:
1. Library Imports and Functions: Loads the dataset into a Pandas DataFrame, displays the first few rows to understand the structure, checks for missing values and basic statistics.
2. Data Loading and Initial Overview: Load the dataset and perform initial data exploration.
3. Data Cleaning: Prepare the dataset for analysis, performing data cleaning and transformation steps, such as: handling missing values, converting `datetime` for time-series analysis, renaiming features for machine learning models.
4. Exploratory Data Analysis (EDA): Analyze the data using visualizations and statistical analysis to uncover trends and relationships between variables. Perform further data cleaning by handling outliers and resampling the data to fix timestamp gaps, ensuring a uniform datetime interval. Analyze the correlation between features to aid in the feature selection process.
5. Machine Learning Models: implement and evaluate a traditional Machine Learning (ML) model and a deep learning ML model to predict nitrate and pH levels in the pond, respectively. Each model makes predictions based on time-series parameters to provide a prediction window of 5 time steps.  
6. Model Deployment: Deploy the train and tested models to generate 5-step predictions for nitrate and pH levels in the pond. These predictions will be used to establish a real-time dashboard for visualizing water quality insights obtained through this notebook. Bridge machine learning modeling with real-time decision-making, ensuring that the insights gained can be effectively utilized for aquaponics system optimization.  


#### License
This project is licensed under the MIT License - see the [LICENSE.txt](LICENSE.txt) file for details.
