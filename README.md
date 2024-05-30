# USA Housing Data Analysis

This project involves analyzing a dataset of housing information in the USA. The analysis includes data exploration, visualization, and building a linear regression model to predict house prices.

## Table of Contents
- [Installation](#installation)
- [Data Description](#data-description)
- [Data Exploration and Visualization](#data-exploration-and-visualization)
- [Model Building](#model-building)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/usa-housing-analysis.git
   ```
2. Navigate to the project directory:
   ```bash
   cd usa-housing-analysis
   ```
3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Data Description

The dataset used in this project is `USA_Housing.csv`. It contains the following columns:
- `Avg. Area Income`: Average income of residents in the area.
- `Avg. Area House Age`: Average age of houses in the area.
- `Avg. Area Number of Rooms`: Average number of rooms in houses in the area.
- `Avg. Area Number of Bedrooms`: Average number of bedrooms in houses in the area.
- `Area Population`: Population of the area.
- `Price`: Price of the houses.

## Data Exploration and Visualization

1. Display the first five rows of the dataset.
2. Display information about the dataset, including data types and null values.
3. Visualize null values in the dataset using a heatmap.
4. Generate descriptive statistics for the dataset.
5. Plot pairwise relationships in the dataset using Seaborn's `pairplot`.
6. Visualize the correlation between features using a heatmap.
7. Display the distribution of house prices.

## Model Building

1. Split the dataset into training and testing sets.
2. Train a linear regression model on the training data.
3. Print the intercept and coefficients of the model.
4. Make predictions on the test data.

## Usage

1. Import necessary libraries:
   ```python
   import pandas as pd
   import numpy as np
   import matplotlib.pyplot as plt
   import seaborn as sns
   from sklearn.model_selection import train_test_split
   from sklearn.linear_model import LinearRegression
   ```

2. Load the dataset:
   ```python
   USA_Housing = pd.read_csv("USA_Housing.csv")
   ```

3. Perform data exploration and visualization.

4. Split the data and train the model:
   ```python
   x = USA_Housing[['Avg. Area Income', 'Avg. Area House Age', 'Avg. Area Number of Rooms',
                    'Avg. Area Number of Bedrooms', 'Area Population']]
   y = USA_Housing['Price']
   x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.4)
   
   ln = LinearRegression()
   ln.fit(x_train, y_train)
   ```

5. Make predictions:
   ```python
   prediction = ln.predict(x_test)
   ```

