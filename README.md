# Algerian Forest Fire Prediction Model

This project involves building a machine learning model to predict the occurrence of forest fires based on meteorological data from two regions in Algeria: Bejaia and Sidi-Bel-Abbes. The goal is to develop a reliable classification model that can help in early detection and prevention efforts.

---
### Workflow

1.  **Data Cleaning & Preprocessing:** The initial dataset was messy, containing two separate data blocks and inconsistent formatting. The data was cleaned by splitting it into the two regions, standardising column names, converting data types, and handling missing values.
2.  **Exploratory Data Analysis (EDA):** I performed EDA to understand the relationships between different weather features and the occurrence of fires. A correlation heatmap was used to identify highly correlated features such as `BUI`, `FWI`, `DMC`, and `DC`.
3.  **Feature Engineering & Selection:** A `Region` column was added, and the target variable `Classes` was encoded into a binary format (1 for 'fire', 0 for 'not fire'). Features were selected for the model, and the data was scaled using `StandardScaler` to prepare it for training.
4.  **Model Building & Evaluation:** I trained and evaluated several classification models, including **Logistic Regression** and **Decision Tree**, to find the best-performing algorithm. The models were rigorously evaluated using key metrics:
    * **Accuracy:** Overall correctness of predictions.
    * **Precision:** The model's accuracy in predicting the 'fire' class.
    * **Recall:** The model's ability to find all actual fire instances.
    * **F1-Score:** The harmonic mean of precision and recall.

---
### Key Findings & Results

The analysis revealed strong correlations between various Fire Weather Index (FWI) system components and the likelihood of a fire. After training and evaluation, the **Decision Tree Classifier** emerged as the most effective model, achieving a high accuracy in predicting fire occurrences.

**Final Model Performance (Random Forest):**
* **Accuracy:** [Enter your highest accuracy score here, e.g., 98%]
* **Precision (for 'fire' class):** [100%]
* **Recall (for 'fire' class):** [94%]

---
### **Dataset Glossary**

#### **Meteorological Data**
* **Temperature**: Temperature in Celsius.
* **RH**: Relative Humidity (%).
* **Ws**: Wind speed (km/h).
* **Rain**: Rain accumulation (mm).

***
#### **Fire Weather Index (FWI) System**
* **FFMC (Fine Fuel Moisture Code)**: Moisture in surface litter. Indicates ease of ignition.
* **DMC (Duff Moisture Code)**: Moisture in the layer below the surface. Indicates medium fuel consumption.
* **DC (Drought Code)**: Moisture in deep soil. A long-term drought indicator.
* **ISI (Initial Spread Index)**: A score for the initial fire spread rate based on wind and FFMC.
* **BUI (Buildup Index)**: Total amount of dry fuel available to burn.
* **FWI (Fire Weather Index)**: Overall score for fire intensity and spread potential.

***
#### **Target Variable**
* **Classes**: The target variable, indicating if a fire occurred (`1`) or not (`0`).

___  
### Technologies Used

* **Python**
* **Pandas** for data manipulation
* **NumPy** for numerical operations
* **Matplotlib & Seaborn** for data visualization
* **Scikit-learn** for model building and evaluation
