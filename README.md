# Social-Media-Stock-Movement-Analysis
### Project Description  

This repository contains the **Stock Movement Analysis** project, which predicts stock trends using social media data **Reddit** through sentiment analysis and machine learning models. It includes a scraper for data collection, preprocessing scripts, and predictive models to analyze stock movements effectively.  

---

### Installation Requirements  

Follow the steps below to set up and run the project, install the following dependencies in order of importance:  

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
#### **. Setup API Keys**  

##### **Step A: Reddit API Configuration**  
1. Create a **config.py** file to securely store your Reddit API credentials:  
   ```python
   with open("config.py", "w") as file:
       file.write('CLIENT_ID = "your_client_id"\n')
       file.write('CLIENT_SECRET = "your_client_secret"\n')
       file.write('USER_AGENT = "your_user_agent"\n')
   ```  
   Replace `your_client_id`, `your_client_secret`, and `your_user_agent` with your actual Reddit API credentials.  

2. Ensure the script imports this configuration:  
   ```python
   from config import CLIENT_ID, CLIENT_SECRET, USER_AGENT
   ```

##### **Step B: Alpha Vantage API Configuration**  
1. Obtain an API key from Alpha Vantage.  
2. Add your Alpha Vantage API key to the script:  
   ```python
   api_key = "your_alpha_vantage_api_key"
   ```
   Alternatively, you can add it to **config.py** for central management:  
   ```python
   with open("config.py", "a") as file:
       file.write('ALPHA_VANTAGE_API_KEY = "your_alpha_vantage_api_key"\n')
   ```

---

#### **3. Run the Scripts**  

1. **Data Scraping:**  
   Use the Reddit API to fetch relevant stock discussion data. Ensure `config.py` is correctly set up to authenticate API calls.

2. **Fetch Historical Stock Prices:**  
   - The script fetches stock price data from Alpha Vantage using the provided `api_key`.  
   - Ensure the stock symbols list and date range are specified correctly.  

3. **Merge Data:**  
   - The fetched stock price data is merged with daily sentiment scores for analysis.  
   - The combined dataset is then processed for machine learning model training.

4. **Train Models:**  
   Run the training scripts to preprocess the data and train the predictive models using the cleaned dataset.

---

#### **Usage Tips**  
- **Organize your directory:** Keep your scripts, data files, and `config.py` in the same directory for seamless execution.  
- **Test your API keys:** Ensure both Reddit and Alpha Vantage API keys are valid and have sufficient quotas for usage.  
- **Modify the configuration:** For multiple users, maintain a template of `config.py` and update keys as required.
- With these instructions, your environment will be ready to scrape data, train models, and predict stock trends.
- Install these libraries before running the scripts or notebooks. These tools are prioritized to ensure seamless data scraping, preprocessing, and predictive modeling, making the workflow efficient and reliable.
