## Algorithm for Ham or Spam Email Classifier

1. **Data Preparation:**
   - Unzip the dataset (e.g., `enron1.zip`) into the current directory.
   - Traverse the dataset folders to read emails categorized as "ham" and "spam."
   - Create a Pandas DataFrame to store email contents and their categories.

2. **Data Cleaning:**
   - Drop unnecessary columns from the DataFrame (e.g., the email filename).
   - Map the categorical labels ("ham" and "spam") to numeric values (0 for ham, 1 for spam).

3. **Text Normalization:**
   - Define a `preprocessor` function that:
     - Replaces all non-alphabet characters with spaces.
     - Converts the text to lowercase.

4. **Feature Extraction:**
   - Instantiate a `CountVectorizer` with the custom `preprocessor`.
   - Split the dataset into training and testing sets using `train_test_split`.

5. **Model Training:**
   - Transform the training text data into a document-term matrix using `fit_transform`.
   - Instantiate a `LogisticRegression` model and fit it to the training data.

6. **Model Evaluation:**
   - Transform the test dataset using the vectorizer.
   - Generate predictions using the trained model.
   - Calculate and print:
     - Accuracy score of the model.
     - Confusion matrix to assess true positives, false positives, etc.
     - Classification report for detailed performance metrics.

7. **Feature Importance Analysis:**
   - Extract feature importance from the model coefficients.
   - Identify and print the top positive (spam-related) and negative (ham-related) features based on importance.

8. **Conclusion:**
   - Summarize findings and results.

This algorithm outlines the steps taken in the notebook to build an email classifier using logistic regression.
