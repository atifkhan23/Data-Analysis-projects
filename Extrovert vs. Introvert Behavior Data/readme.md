Extrovert vs. Introvert Behavior Feature Importance Analysis
Overview
This project performs feature importance analysis on the Extrovert vs. Introvert Behavior Dataset using a Random Forest Classifier. The goal is to identify which features are most predictive of personality types (Extrovert or Introvert). The script processes the dataset, handles missing values, encodes categorical variables, trains a Random Forest model, and outputs feature importances in a text-based tabular format.
Dataset

Source: Extrovert vs. Introvert Behavior Data on Kaggle
Description: The dataset contains features related to personality traits and a target column 'Personality' indicating whether an individual is an Extrovert or Introvert.
File: extrovert_vs_introvert_behavior_data.csv (download from Kaggle and place in the project directory).

Requirements

Python 3.8+
Libraries listed in requirements.txt (install using pip install -r requirements.txt)

Setup

Download the Dataset:

Visit the Kaggle dataset page and download extrovert_vs_introvert_behavior_data.csv.
Place the file in a directory (e.g., data/).


Install Dependencies:
pip install -r requirements.txt


Update File Path:

Open extrovert_introvert_feature_importance.py.
Replace 'path_to_dataset/extrovert_vs_introvert_behavior_data.csv' with the actual path to the dataset (e.g., 'data/extrovert_vs_introvert_behavior_data.csv').



Running the Code
Execute the Python script:
python extrovert_introvert_feature_importance.py

Output
The script prints:

Confirmation of dataset loading and 'Personality' column presence.
Missing value summary and handling confirmation.
Random Forest training status.
A sorted table of feature importances (feature name and importance score).
Dataset info (shape and 'Personality' value counts).

Example output:
Dataset loaded successfully.
Columns in dataset: ['social_interaction', 'energy_level', 'communication_style', 'group_preference', 'decision_making', 'openness', 'Personality']
Confirmed: 'Personality' column is present.

Checking for missing values...
social_interaction       0
energy_level            0
communication_style     0
group_preference        0
decision_making         0
openness                0
Personality             0
dtype: int64
Missing values handled.
Random Forest model trained successfully.

=== Feature Importance for Personality Prediction ===
Feature                        Importance
---------------------------------------------
social_interaction             0.3500
energy_level                   0.2500
communication_style            0.2000
group_preference               0.1000
decision_making                0.0700
openness                       0.0300

=== Dataset Info ===
Shape: (1000, 7)
Target value counts:
Extrovert    520
Introvert    480
Name: Personality, dtype: int64

Troubleshooting

No Output: Check the console for error messages (e.g., file not found, encoding errors).
File Not Found: Ensure the dataset path in the script is correct.
Missing 'Personality' Column: Verify the column name is exactly 'Personality' (case-sensitive) using print(df.columns).
Data Issues: Add print(df.head()) or print(df['Personality'].unique()) to inspect the data.

License
This project is licensed under the MIT License.
