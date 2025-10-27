# ⚽ Foul Classifier – AI Project
## Group Name: Team Codex

#### 👥 Group Members

| Name                       | Matriculation Number |
|-----------------------------|----------------------|
| John O. Nathaniel       | VUG/CSC/23/8862      |
| Anointed Rademene Ekabua    | VUG/CSC/23/8883      |
| Adashi Olabi Odey           | VUG/CSC/23/8992      |
| Joseph Dzarma             | VUG/CSC/23/8863      |
| Toby Amachree             | VUG/CSC/23/8927         |
| Angoewelba  Benjamin  Dayil | VUG/CSC/23/9798        |
| Ogbonna Kingmiracle           | VUG/CSC/23/9482       |
| Makanjuola Samuel             | VUG/CSC/23/9806       |
| Oyekale Timileyin Dorcas      | VUG/CSC/23/9245       |
| Adnan Emmanuel Garba          | VUG/CSC/23/10056      |
| Ugbede Favour Ufedo           | VUG/CSC/23/9311       |
| Kwallu K. Kenneth             | VUG/VUG/22/8470       |
| Solomon Victor Eneiramo       | VUG/CSC/23/8942       |
| Onu Alex Kelvin               | VUG/CSC/23/9176       |
| Datong Wallat Danielle        | VUG/CSC/23/9618       |
| Success Mbah                  | VUG/CSC/23/10185      |
| Temitayo Nuhu Adesalam        | VUG/CSC/23/8849       |
| Njoku C. Junior Julian        | VUG/CSC/23/8857       |
| David Agweye                  | VUG/csc/23/9479       |
| Akuagwu Eurial                | VUG/CSC/23/9359       |
| Angoewelba Benjamin Dayil     | VUG/CSC/23/9798       |
| Benjamin Annick Chizitere     | VUG/CSC/23/8817       |
| Adnan Emmanuel Garba          | VUG/CSC/23/10056      |
| Nudamu Hyacinth Dagala        | VUG/CSC/23/9558       |
| Shalangwa Mosisienemo Hyeladi | VUG/CSC/23/9248       |
| Gideon O. Reuben              | VUG/CSC/24/13302      |
| Abubakar Maryam               | VUG/CSC/23/8903       |
| Kanayo Chukwunweike           | VUG/CSC/22/8570       |
| Ojabo David                   | VUG/CSC/23/8886       |
| Okereke perfect               | VUG/CSC/23/9350       |
| Dim Chidera Emmanuel          | VUG/CSC/24/12772      |
| Omata Joseph                  | VUG/CSC/23/10653      |
| Godson Kingzion               | VUG/CSC/23/10031      |
| Samuel Asuquo                 | VUG/CSC/23/10193      |


## 🎯 Project Objectives


This project aims to use machine learning to predict whether a football event is a foul or not using real match data.
We worked with the Kaggle Football Events dataset, which contains detailed play-by-play records of professional football games.
Our goal was to train and compare different models to see which best detects fouls based on patterns like event type, situation, and location on the pitch.

## ⚙️ Summary of Approach and Results
1. Dataset Preparation

- We cleaned the dataset and handled missing values by filling them with "Unknown".

- Created a target column is_foul, where foul-related events were labeled 1, and others were labeled 0.

- Simplified the field locations into Defensive, Midfield, Attack_Wide, and Attack_Central zones.

- Encoded categorical columns using LabelEncoder to make them numeric.

2. Feature Engineering

- We added new features to give the models more context:

- `match_phase` (Early, Mid, Late match)

- `is_attack_situation` (Corner or free kick)

- `is_head_involved` (If the player used their head)

- `is_fast_attack_zone` (If event happened during a fast break)

3. Models Used

- We trained and compared three models:

- Random Forest (RF1): Baseline model with original features.

- Random Forest (RF2): Improved model with engineered features.

- XGBoost: Advanced boosting model for higher accuracy and interpretability.

4. Results

- F1 Score: ~0.88

- Accuracy: ~0.85

- ROC-AUC: ~0.93

All three models performed similarly, showing that our features and preprocessing were effective.
The XGBoost model also provided a feature importance chart that showed situation, event_type2, and location_group were the most influential in predicting fouls.

## 📊 Key Insights

- Most fouls occurred during set-piece or attacking situations.

- The match situation and location on the field were the strongest indicators of fouls.

- Feature engineering didn’t drastically change accuracy but made the model more interpretable and realistic.

## 🧠 Instructions on How to Run the Code
1. Setup Environment

    Make sure you have Python 3.10+ installed.
    Then install dependencies using:

        pip install -r requirements.txt

2. Run Notebook

    Open the Jupyter or Google Colab notebook:

    Foul Classifier.ipynb


    The code will:

    - Automatically download the Kaggle dataset via kagglehub

    - Preprocess and clean the data

    - Train all three models

    - Display performance metrics and feature importance graphs

3. Output

    After running, the notebook prints:

        - F1, Accuracy, and ROC-AUC scores

        - Visualizations (confusion matrix & feature importance chart)

## 📘 Summary

This project demonstrates how AI and machine learning can be applied to sports analytics.
We successfully built and compared models capable of detecting fouls using football match data — proving that with clean data and feature engineering, AI can help improve referee decisions, player analysis, and match strategy.#
