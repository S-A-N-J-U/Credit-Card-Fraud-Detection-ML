# Credit Card Fraud Detection

This repository contains code for building a credit card fraud detection system using machine learning techniques. The dataset used for this project is the Credit Card Fraud Detection dataset, which contains anonymized credit card transactions labeled as fraudulent or legitimate.

## Dataset

The dataset used for this project is available in the `creditcard.csv` file. It contains the following columns:

- `Time`: Time elapsed in seconds since the first transaction
- `V1-V28`: Anonymized features resulting from a PCA transformation
- `Amount`: Transaction amount
- `Class`: Class label indicating whether the transaction is fraudulent (1) or legitimate (0)

The dataset consists of 284,807 transactions, with 492 fraudulent transactions and 284,315 legitimate transactions. It is highly imbalanced, with fraudulent transactions representing a small portion of the data.

## Data Exploration

The code provided performs initial data exploration to gain insights into the dataset. It includes the following steps:

1. Loading the dataset using Pandas.
2. Checking the structure and summary statistics of the dataset.
3. Verifying the presence of missing values (there are none in this case).
4. Examining the distribution of legitimate and fraudulent transactions.
5. Calculating statistical measures for the transaction amounts in both classes.
6. Comparing the mean values of the features for legitimate and fraudulent transactions.

## Under-Sampling Technique

To address the class imbalance, an under-sampling technique is employed. The code performs the following steps:

1. Creating a sample dataset with a similar distribution of legitimate and fraudulent transactions.
2. Randomly selecting a subset of legitimate transactions equal to the number of fraudulent transactions (492).
3. Concatenating the selected legitimate transactions with the fraudulent transactions to create a new balanced dataset.

## Code

```python
import pandas as pd
import numpy as np
from sklearn.utils import shuffle

# Load the dataset
data = pd.read_csv("creditcard.csv")

# Data exploration
# ...

# Under-sampling technique
# ...

# Further code implementation...
```
## Usage
To use this code, follow these steps:

1. Unzip the `creditcard.csv.zip` file located in the `CC_Fraud_Detection` directory.
2. Execute the provided code in a Python environment with the required dependencies (NumPy, Pandas, scikit-learn).
3. The code will load the dataset, perform data exploration, and generate a new balanced dataset using under-sampling.
4. You can further build upon this code to develop a fraud detection model or perform additional analysis.
Note: Make sure to adjust the file paths if necessary.

Feel free to modify and enhance the code according to your specific requirements.

## License
This project is licensed under the MIT License.
