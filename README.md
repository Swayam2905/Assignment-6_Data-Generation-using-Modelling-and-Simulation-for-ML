**🔬 Cantera-Based Chemical Reaction Simulation with Machine Learning**
**📌 Project Overview**

This project integrates chemical kinetics simulation with machine learning to study and predict the reaction rate of ammonia (NH₃) as a function of temperature and pressure.

Chemical reaction data is generated using the Cantera library with the GRI-Mech 3.0 mechanism, and multiple regression models are trained to predict the NH₃ production rate.

**🎯 Objectives**

Simulate NH₃ reaction behavior using physics-based chemical modeling

Generate a dataset by varying temperature and pressure

Train and compare different machine learning regression models

Evaluate model performance using standard metrics

**🧪 Tools & Technologies Used**

Python

Cantera – chemical kinetics simulation

NumPy – numerical operations

Pandas – data handling

Scikit-learn – machine learning models & evaluation

**⚙️ Chemical Simulation Details**
Parameter	Value
Reaction mechanism	gri30.yaml
Target species	NH₃ (Ammonia)
Temperature range	−40 °C to 40 °C
Pressure range	10 atm to 50 atm
Reacting mixture	N₂ : H₂ = 1 : 3
Samples generated	1000

The reacting gas composition is explicitly defined to enable NH₃ formation.

**📊 Dataset Description**

The generated dataset contains the following columns:

Column Name	Type	Description
Temperature_C	Input	Temperature in Celsius
Pressure_atm	Input	Pressure in atmospheres
Reaction_Rate	Output	Absolute net production rate of NH₃

Input Features: Temperature_C, Pressure_atm

Output / Target: Reaction_Rate

The dataset is saved as:

cantera_simulated_data.csv

**📤 Output Description**

The Reaction_Rate column represents the absolute net production rate of NH₃, calculated using Cantera’s chemical kinetics solver for the specified reacting mixture.

This value is used as the target variable for all machine learning models.

**🤖 Machine Learning Models Used**

The following regression models are implemented and compared:

Linear Regression

Decision Tree Regressor

Random Forest Regressor

Support Vector Regression (SVR)

K-Nearest Neighbors (KNN)

Feature scaling is applied for SVR and KNN to ensure correct learning behavior.

**📈 Model Evaluation Metrics**

Each model is evaluated using:

Mean Squared Error (MSE)

R² Score

The results are presented in a comparative table after training.

**▶️ How to Run the Project**
1️⃣ Install Required Libraries
pip install cantera numpy pandas scikit-learn

2️⃣ Run the Python Script / Notebook

Execute the code to:

Load the chemical mechanism

Generate simulation data

Save the dataset

Train ML models

Display performance metrics

**Result Table**

<img width="451" height="156" alt="image" src="https://github.com/user-attachments/assets/f65256a6-4f71-4d6b-8677-4d0151a3112b" />


**🧠 Key Learning Insight**

Initial simulations produced zero NH₃ reaction rates because the gas composition was not defined. After specifying a nitrogen–hydrogen reacting mixture, meaningful reaction rates were obtained, enabling effective machine learning modeling.

**🚀 Future Enhancements**

Hyperparameter tuning of ML models

Visualization of reaction trends

Extension to multiple chemical species

Deep learning–based regression

Sensitivity analysis

**👤 Author**

Swayam Gupta
