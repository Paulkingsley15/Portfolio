# Basketball Shot Log Analysis

## Introduction

This project contains a Jupyter Notebook that analyzes basketball shot log data. The primary goal is to derive insights into player shooting performance, shot selection, and the factors affecting the success or failure of shots. The notebook includes data preprocessing, exploratory data analysis (EDA), and statistical modeling to predict or understand shooting outcomes.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Methods](#methods)
4. [Results](#results)
5. [How to Run](#how-to-run)
6. [Dependencies](#dependencies)

## Project Overview

The basketball shot log dataset contains detailed information on individual shots taken during games. The objective is to analyze shooting patterns, player tendencies, and the conditions that influence shot success rates. The project implements data analysis techniques to visualize and understand the impact of various factors such as shot distance, defender presence, and shot type.

## Dataset

- **Source**: The dataset used for this project is titled `updated_shot_logs.csv`.
- **Features**:
  - `GAME_ID`: Unique identifier for each game
  - `MATCHUP`: Matchup information for the game
  - `PLAYER_ID`: Unique identifier for each player
  - `PLAYER_NAME`: Name of the player taking the shot
  - `SHOT_NUMBER`: Sequential number of the shot for the player in the game
  - `PERIOD`: Period of the game in which the shot occurred
  - `GAME_CLOCK`: Time remaining in the game or period when the shot was taken
  - `SHOT_CLOCK`: Time remaining on the shot clock
  - `DRIBBLES`: Number of dribbles before the shot
  - `TOUCH_TIME`: Time in seconds the player had possession before the shot
  - `SHOT_DIST`: Distance of the shot in feet
  - `PTS_TYPE`: Whether the shot was for 2 or 3 points
  - `SHOT_RESULT`: Result of the shot (made or missed)
  - `CLOSE_DEF_DIST`: Distance of the closest defender in feet
  - `FGM`: Field goal made (1 if made, 0 if missed)
  - `PTS`: Points scored on the shot
  - `LOCATION`: Whether the game is home or away
  - `W`: Whether the player's team won (W) or lost (L) the game
  - Additional features depending on the dataset specifics.

- **Size**: The dataset consists of several thousand records with [X] rows and [Y] columns.

## Methods

- **Data Preprocessing**:
  - Handling missing or erroneous values in columns like `SHOT_CLOCK` or `CLOSE_DEF_DIST`.
  - Encoding categorical variables like `PLAYER_NAME`, `MATCHUP`, and `SHOT_RESULT`.
  - Feature engineering to create new variables such as `SHOT_MADE_FLAG` based on `SHOT_RESULT`.

- **Exploratory Data Analysis (EDA)**:
  - Visualizing the distribution of shot attempts based on different shot distances and shot clock times.
  - Analyzing the success rate of shots based on defender proximity (`CLOSE_DEF_DIST`).
  - Identifying correlations between game context (period, game clock, location) and shot success.

- **Modeling**:
  - Predictive models are applied to understand the factors that impact shot success, such as:
    - Logistic Regression to predict the probability of a shot being made.
    - Random Forest or Decision Trees to explore feature importance for shot success.
  - Performance metrics include accuracy, precision, recall, and AUC (for classification models).

## Results

- **Key Insights**:
  - Players tend to have higher shooting accuracy at closer distances, as expected.
  - Defender proximity (`CLOSE_DEF_DIST`) plays a significant role in shot success rates.
  - Time remaining on the shot clock and period of the game also impact shooting efficiency.
  - [Model performance] with metrics like accuracy, precision, and recall can help predict shot outcomes based on game situations and player behavior.

## How to Run

1. **Install Required Dependencies**:
   Ensure you have the required Python libraries installed:
   ```bash
   pip install jupyter pandas scikit-learn matplotlib seaborn
   
Run the Notebook: Open the notebook using Jupyter:

bash
Copy code
jupyter notebook "basketball 2.ipynb"
Follow the instructions in the notebook to execute the cells sequentially.

Data Processing:

The notebook loads the updated_shot_logs.csv file and processes the data, including handling missing values and transforming features for model input.
EDA is performed to visualize the data and understand its structure.
Machine Learning:

Machine learning models are built to predict the likelihood of shot success (SHOT_RESULT).
The results of each model are evaluated using accuracy, precision, recall, and AUC.
Dependencies
Python 3.x
Jupyter Notebook
Pandas
NumPy
Scikit-learn
Matplotlib
Seaborn
