# Social-Media-Stock-Movement-Analysis
### Project Description  

This repository contains the **Stock Movement Analysis** project, which predicts stock trends using social media data **Reddit** through sentiment analysis and machine learning models. It includes a scraper for data collection, preprocessing scripts, and predictive models to analyze stock movements effectively.  

---

### Installation Requirements  

To set up the project, install the following dependencies in order of importance:  

1. **praw**: Python Reddit API Wrapper, essential for scraping Reddit data related to stock discussions.  
   - Install: `pip install praw`  

2. **pandas**: For data manipulation and analysis during preprocessing and model evaluation.  
   - Install: `pip install pandas`  

3. **re**: Used for text preprocessing tasks like cleaning and formatting social media data.  
   - Included in Python's standard library.  

4. **nltk**: For natural language processing, such as removing stopwords and preparing text for analysis.  
   - Install: `pip install nltk`  
   - Command: `from nltk.corpus import stopwords`  

5. **vaderSentiment**: A sentiment analysis tool that evaluates the sentiment of text from social media platforms.  
   - Install: `pip install vaderSentiment`  

6. **scikit-learn**: A machine learning library providing essential tools for model building, evaluation, and hyperparameter tuning.  
   - Install: `pip install scikit-learn`  
   - Includes:  
     - `LogisticRegression`: A simple classification model for binary or multiclass prediction.  
     - `RandomForestClassifier`: A robust ensemble-based model.  
     - `GridSearchCV`: For hyperparameter tuning.  
     - `train_test_split`: Splits data into training and testing sets.  
     - Metrics: `accuracy_score`, `precision_score`, `recall_score`, `f1_score`, and `confusion_matrix`.  

7. **xgboost**: A high-performance gradient boosting library for advanced predictive modeling.  
   - Install: `pip install xgboost`  

8. **numpy**: Used for numerical computations and array handling.  
   - Install: `pip install numpy`  

9. **MLPClassifier**: A neural network model for classification tasks, included in `scikit-learn`.  

---

### Usage  
Install these libraries before running the scripts or notebooks. These tools are prioritized to ensure seamless data scraping, preprocessing, and predictive modeling, making the workflow efficient and reliable.
