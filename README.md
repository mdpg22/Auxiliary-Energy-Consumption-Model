# 🚄 Auxiliary Energy Consumption Modeling in Railway Systems

Industrial Data Science project focused on modeling and predicting
auxiliary AC energy consumption in railway systems using regression
analysis and Machine Learning techniques.

------------------------------------------------------------------------

## 🎯 Project Objective

The goal of this project is to model the energy consumption of auxiliary
systems connected to the AC branch of a railway converter.

Specifically:

-   Model auxiliary energy consumption (kWh) as a function of HVAC and
    compressor operating times.
-   Compare energy consumption across different event types
    (interstation vs stop).
-   Develop a linear regression model for explainability.
-   Validate the model using RMSE.
-   Develop a more complex Machine Learning model and compare predictive
    performance.

------------------------------------------------------------------------

## 📂 Dataset Description

The dataset contains one month of operational data (September 2019),
aggregated by event type:

Events: - interstation - stop - maintenance (removed during filtering)

Main variables:

-   `eaux_train_ac` → Energy consumed in AC branch \[kWh\]
-   `event_duration` → Event duration \[s\]
-   `suma_ton_compresores` → Compressor operating time \[s\]
-   `suma_hvac_ton_compresores` → HVAC room compressor time \[s\]
-   `suma_hvac_ton_heater` → HVAC room heater time \[s\]
-   `suma_ton_comp_cab` → Cabin HVAC compressor time \[s\]
-   `suma_ton_heater_cab` → Cabin HVAC heater time \[s\]

Filtering applied:

-   Events longer than 600 seconds removed
-   Maintenance events removed

------------------------------------------------------------------------

## 🛠 Technologies Used

-   Python / R (depending on implementation)
-   pandas / tidyverse
-   scikit-learn / base regression tools
-   numpy
-   matplotlib / seaborn

------------------------------------------------------------------------

## 🔎 Project Structure

auxiliary-energy-consumption-modeling/ 
│ 
├── Entrega_1.ipynb #Main Analysis
├── Entregable1.RData #Dataset
├── 2025_Entregable1_Equipo_Auxiliares.pdf #Documentation and information
└── README.md

------------------------------------------------------------------------

## 📊 Methodology

### 1️⃣ Data Loading & Filtering

-   Load dataset from RData
-   Remove maintenance events
-   Remove events \> 600 seconds

------------------------------------------------------------------------

### 2️⃣ Exploratory Analysis

-   Compare energy consumption between event types
-   Statistical comparison (significance testing)
-   Power comparison (kW derived from kWh / time)

------------------------------------------------------------------------

### 3️⃣ Linear Regression Model

Model form:

E_aux = β0 + β1·x1 + β2·x2 + ... + βn·xn

Where:

-   Target variable → `eaux_train_ac`
-   Predictors → Operating times of compressors and HVAC systems

Training: - First half of September data

Validation: - Second half of September data

Evaluation metric: - RMSE

Key aspects analyzed:

-   Statistical significance of coefficients
-   Interpretation of regression coefficients
-   Residual distribution
-   Model generalization

------------------------------------------------------------------------

### 4️⃣ Advanced Machine Learning Model

A more complex ML model was trained using the same training subset and
validated on the same validation subset.

Comparison performed between:

-   Linear regression (high explainability)
-   ML model (higher predictive complexity)

Evaluation:

-   RMSE (train vs validation)
-   Overfitting analysis
-   Trade-off between performance and explainability

------------------------------------------------------------------------

## 📈 Key Insights

-   Auxiliary energy consumption can be reasonably modeled using
    component operating times.
-   Linear regression provides interpretability in terms of estimated
    average power per component.
-   More complex ML models may improve predictive performance but reduce
    interpretability.
-   Model validation using RMSE is critical to assess real-world
    deployment feasibility.

------------------------------------------------------------------------

## 🚀 How to Run

1.  Clone repository:

git clone
https://github.com/yourusername/auxiliary-energy-consumption-modeling.git

2.  Install required dependencies.

3.  Open:

Entrega_1.ipynb

4.  Run notebook to reproduce modeling process.

------------------------------------------------------------------------

## 🏭 Industrial Context

This project was developed in an industrial railway context (CAF I+D)
and focuses on practical modeling of auxiliary system energy
consumption.

------------------------------------------------------------------------

## 📚 Academic Context

Master's level coursework in Industrial & Intelligent Systems with focus
on applied Machine Learning and Energy Modeling.

------------------------------------------------------------------------

## 📬 Author

Manuel de Prado García\
Master Data Analysis in Engineering\
Specialization in AI, Data Science & Data Anlysis
