# Spam Mail Detection Using Python

## Overview
This project implements a simple spam mail detection system using Python and machine learning techniques. The code utilizes the scikit-learn library for machine learning tasks and pandas for data manipulation. The model is based on logistic regression and employs the TF-IDF (Term Frequency-Inverse Document Frequency) vectorization technique to convert text data into numerical features.

## Code Structure
The code is organized into the following sections:

1. **Data Loading and Preprocessing:**
   - The dataset is loaded using pandas from a CSV file (`mail_data.csv`).
   - Initial exploration of the dataset is performed using `head()`, `info()`, and `isnull().sum()` functions.
   - Null values in the dataset are replaced with empty strings.
   - A binary classification is created for the 'Category' column, where 'ham' is labeled as 1 (not spam) and others as 0 (spam).
   - Unnecessary columns like 'Category' are dropped.

2. **Data Splitting:**
   - The data is split into training and testing sets using `train_test_split` from scikit-learn.

3. **Text Vectorization:**
   - TF-IDF vectorization is applied to convert the text data into feature vectors. The `TfidfVectorizer` is configured to ignore English stop words and convert all text to lowercase.

4. **Model Training:**
   - A logistic regression model is employed for training using the transformed training data.

5. **Model Evaluation:**
   - The accuracy of the model is evaluated on both the training and testing datasets.

6. **Prediction:**
   - The model is used to predict the category of a new input mail. The input mail is first transformed using the same TF-IDF vectorizer, and the model predicts whether it is spam or not.

## How to Use
1. **Clone the Repository:**
   ```
   git clone https://github.com/your-username/Spam-Mail-Detection-Using-Python.git
   cd Spam-Mail-Detection-Using-Python
   ```

2. **Install Dependencies:**
   ```
   pip install pandas numpy scikit-learn
   ```

3. **Run the Code:**
   - Ensure that the `mail_data.csv` file is present in the same directory.
   ```
   python spam_mail_detection.py
   ```

4. **Modify Input:**
   - You can modify the `input_your_mail` variable with your own email content for testing.

5. **Review Results:**
   - The code will print the accuracy on both the training and testing datasets.
   - It will also predict whether the input mail is spam or ham.

## Notes
- The dataset used (`mail_data.csv`) should have a 'Category' column indicating whether the mail is 'ham' or 'spam'.
- Ensure that the necessary libraries are installed using the provided requirements file.

Feel free to customize and extend this project according to your needs!
