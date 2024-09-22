# SMS-Classifier_NB

This project involves building a machine learning model to classify SMS messages as either “spam” or “ham” (not spam). The dataset used contains 5,572 SMS messages, labeled as either “spam” or “ham.” The goal is to preprocess the data, explore it, and build a model that can accurately predict spam messages.

Project Steps:

1. Data Loading and Cleaning

	•	Dataset: The SMS dataset was loaded from a CSV file (spam.csv). The dataset initially had 5 columns, but only two were relevant: v1 (target) and v2 (text).
	•	Cleaning: Unnecessary columns were removed, and the dataset was cleaned by:
	•	Renaming columns for clarity (v1 → target, v2 → text).
	•	Removing 403 duplicate entries.
	•	Encoding the target column to binary (0 for ham and 1 for spam).

2. Exploratory Data Analysis (EDA)

	•	Basic Stats: The dataset was analyzed to understand the distribution of spam vs. ham messages.
	•	Visualization:
	•	Plotted the distribution of message lengths, word counts, and sentence counts.
	•	Generated word clouds for both spam and ham messages to visualize common words in each category.

3. Feature Engineering

	•	Text Transformation:
	•	All text was converted to lowercase and tokenized.
	•	Stopwords and punctuation were removed.
	•	Words were stemmed to their root forms using the PorterStemmer.
	•	Feature Creation:
	•	Three new features were created: the number of characters, words, and sentences in each message.

4. Model Building

Several machine learning algorithms were evaluated, including:

	•	Naive Bayes (MultinomialNB)
	•	Logistic Regression
	•	Support Vector Classifier (SVC)
	•	K-Nearest Neighbors (KNN)
	•	Decision Tree Classifier
	•	Random Forest Classifier
	•	AdaBoost
	•	Bagging Classifier
	•	Gradient Boosting Classifier
	•	XGBoost

Best Performing Models:

	•	Multinomial Naive Bayes: Accuracy = 97.1%, Precision = 1.0
	•	Random Forest Classifier: Accuracy = 97.6%, Precision = 98.3%
	•	Support Vector Classifier (SVC): Accuracy = 97.6%, Precision = 97.5%

5. Model Evaluation

	•	Metrics: Accuracy, precision, and confusion matrices were used to evaluate model performance.
	•	Comparison: A performance comparison of all models was conducted, with Naive Bayes achieving the highest precision, and Random Forest and SVC providing the best overall accuracy.

6. Visualizing Model Performance

	•	Plotted the accuracy and precision of each model to compare their performances.
