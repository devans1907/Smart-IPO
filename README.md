# Smart IPO: Predicting IPO Listing Gains in the Indian Market

This project builds a deep learning classification model to predict whether an Initial Public Offering (IPO) in the Indian market will result in listing gains (i.e., a positive return on the day of listing).

## Problem Statement

An investment firm is interested in identifying IPOs likely to yield listing gains. Using historical IPO data from the Indian market, we aim to develop a model that classifies IPOs as profitable or not on their listing day.

## Dataset

- **Source:** Moneycontrol (Indian IPO data)
- **Rows:** 319
- **Columns:** 9

### Data Dictionary

| Column                | Description                                                        |
|-----------------------|--------------------------------------------------------------------|
| Date                  | Date when the IPO was listed                                       |
| IPOName               | Name of the IPO                                                    |
| Issue_Size            | Size of the IPO issue (INR Crores)                                 |
| Subscription_QIB      | QIB (Qualified Institutional Buyer) subscription count             |
| Subscription_HNI      | HNI (High Networth Individual) subscription count                  |
| Subscription_RII      | RII (Retail Individual Investors) subscription count               |
| Subscription_Total    | Total subscription count                                           |
| Issue_Price           | IPO issue price (INR)                                              |
| Listing_Gains_Percent | % gain in listing price over issue price                           |

## Approach

1. **Data Cleaning & Exploration**
   - Checked for missing values and outliers.
   - Converted `Listing_Gains_Percent` into a binary target variable:  
     - `1` if gain > 0, else `0`.
   - Dropped non-predictive columns.

2. **Visualization**
   - Explored distributions and relationships between variables.
   - Treated outliers using the interquartile range (IQR) method.

3. **Feature Engineering**
   - Normalized predictor variables.

4. **Modeling**
   - Built a deep learning model using TensorFlow/Keras.
   - Architecture: 4 hidden layers (ReLU), 1 output layer (Sigmoid).
   - Loss: Binary Crossentropy  
   - Optimizer: Adam

5. **Evaluation**
   - Used a 70:30 train-test split.
   - Achieved ~75% accuracy on training data and ~69% on test data.

**Contributors:**  
- Devans Daga
