# ChatGPT_Sentiment_Analysis_CODXO_Internship
### 1. Data Loading
- Loaded the dataset from a CSV file.
https://www.kaggle.com/datasets/charunisa/chatgpt-sentiment-analysis

### 2. Data Exploration
- Displayed the total rows and columns in the dataset: `(219294, 3)`.
- Displayed the columns: `['Unnamed: 0', 'tweets', 'labels']`.
- Displayed the first few rows of the dataset.
- Checked for missing values: No missing values found.

### 3. Data Cleaning
- Cleaned the text data by:
  - Removing URLs.
  - Removing mentions and hashtags.
  - Removing special characters and numbers.
  - Converting text to lowercase.
- Removed stop words from the text data.

### 4. Data Visualization
- Visualized the distribution of sentiment labels using a count plot.
- Generated word clouds for each sentiment category to visualize the most common words.

### 5. Feature Extraction
- Used TF-IDF vectorization to convert text data into numerical features, limiting to the top 5000 features.

### 6. Data Splitting
- Split the data into training and testing sets with an 80-20 split.

### 7. Model Building and Evaluation

#### Logistic Regression
1. **Cross-Validation**:
   - Applied 5-fold cross-validation.
   - Cross-validation scores: `[0.82665945, 0.82155784, 0.82543392, 0.82221336, 0.8245504]`.
   - Average cross-validation score: `0.824082993701371`.

2. **Training and Evaluation**:
   - Trained the Logistic Regression model on the training data.
   - Evaluated the model on the test data.
   - Classification report showed good precision, recall, and F1-scores across sentiment categories.
   - Confusion matrix indicated a high number of correct predictions for each category.

3. **Hyperparameter Tuning**:
   - Conducted GridSearchCV to find the best hyperparameters.
   - Best parameters found: `{'C': 10, 'solver': 'lbfgs'}`.

#### Random Forest
1. **Training and Evaluation**:
   - Trained the Random Forest model on the training data.
   - Evaluated the model on the test data.
   - Classification report showed slightly lower performance compared to Logistic Regression.
   - Confusion matrix indicated more misclassifications compared to Logistic Regression.

### Results Summary
- **Logistic Regression**:
  - Cross-validation accuracy: 82.4%
  - Test accuracy: 83%
  - Best hyperparameters: `{'C': 10, 'solver': 'lbfgs'}`

- **Random Forest**:
  - Test accuracy: 79%

### Conclusion
- Logistic Regression performed better than Random Forest in terms of both cross-validation and test accuracy.
- Hyperparameter tuning further optimized the Logistic Regression model.
- The overall accuracy and performance metrics suggest that Logistic Regression is a suitable model for this sentiment analysis task.
