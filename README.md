# Database Query Optimization with Dynamic and Predictive Sharding
This project demonstrates how to optimize database query performance using dynamic sharding and predictive sharding strategies. It leverages an Artificial Neural Network (ANN) to predict whether a query will exceed a certain execution time threshold and simulates sharding adjustments based on resource usage and predicted data growth.

## Table of Contents
- Overview
- Features
- Installation
- Usage
- Code Structure
- Results
- Contributing
- License

## Overview
The goal of this project is to optimize database query performance by:

1. Predicting Query Execution Time: Using an ANN to predict whether a query will exceed a certain execution time threshold (Execution Time (s) > 2.0).
2. Dynamic Sharding: Adjusting shards in real-time based on query load and resource usage (e.g., CPU usage, execution time).
3. Predictive Sharding: Proactively adjusting shards based on predicted data growth.

The project uses a synthetic dataset (synthetic_dataset.csv) to simulate query logs, execution times, and resource usage.

## Features
- Machine Learning Model: An ANN is used for binary classification to predict whether a query will exceed the execution time threshold.
- Dynamic Sharding: Queries are moved to new shards if their execution time or CPU usage exceeds predefined thresholds.
- Predictive Sharding: Shards are adjusted based on predicted data growth using linear regression.
- Visualizations: Includes visualizations for:
  - Confusion Matrix
  - ROC Curve
  - Distribution of Predicted Probabilities
  - Query Distribution Across Shards

 ## Installation
 ### Prerequisites
- Python 3.8 or higher

- Required Python libraries: `pandas`, `numpy`, `scikit-learn`, `tensorflow`, `matplotlib`, `seaborn`

### Steps
1. Clone the repository:

`git clone https://github.com/your-username/database-query-optimization.git
cd database-query-optimization`

2. Install the required libraries:

`pip install -r requirements.txt`

3. Download the dataset (`synthetic_dataset.csv`) and place it in the project directory.

## Usage
1. Run the ipynb
2. Load the dataset.

3. Train the ANN model.
    - Evaluate the model using accuracy, precision, recall, and F1 score.
    - Simulate dynamic and predictive sharding.
    - Generate visualizations.
  
## Code Structure
- Data Loading:

    -The dataset is loaded using pandas.

    - A binary target variable (Target) is created based on the execution time threshold.

- Feature Engineering:

    - Features include Data Size (MB), CPU Usage (%), Memory Usage (MB), and I/O Operations.

    - Features are standardized using StandardScaler.

- Model Training:

    - An ANN is built using TensorFlow/Keras with:

      - Input layer: 64 neurons, ReLU activation.

      - Hidden layer: 32 neurons, ReLU activation.

      - Output layer: 1 neuron, sigmoid activation.

    - The model is trained for 100 epochs with a batch size of 32.

- Evaluation:

    - The model is evaluated using accuracy, precision, recall, and F1 score.

    - A confusion matrix and ROC curve are generated.

- Sharding Simulation:

    - Dynamic Sharding: Queries are moved to new shards if their execution time or CPU usage exceeds thresholds.

    - Predictive Sharding: Shards are adjusted based on predicted data growth.

- Visualizations:

    - Confusion Matrix

    - ROC Curve

    - Distribution of Predicted Probabilities

    - Query Distribution Across Shards

 # Results
 ## Evaluation Metrics
- Accuracy: 0.92

- Precision: 0.89

- Recall: 0.85

- F1 Score: 0.87

## Visualizations
1. Confusion Matrix
2. ROC Curve
3. Distribution of Predicted Probabilities
4. Query Distribution Across Shards

# Acknowledgments
- Dataset: Synthetic dataset generated for demonstration purposes.

- Libraries: `pandas`, `numpy`, `scikit-learn`, `tensorflow`, `matplotlib`, `seaborn`.
