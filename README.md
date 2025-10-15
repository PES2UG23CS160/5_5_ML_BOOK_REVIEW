Book Review Popularity Classifier
Project Description
This project is an NLP-focused solution designed to predict the popularity of book reviews based on their text content. It uses a machine learning pipeline to preprocess textual data, train various classifiers, and evaluate their performance. The main goal is to build an accurate model that can classify reviews as "popular" or "not popular" and to identify the key linguistic features that drive popularity. This project was developed as a machine learning assignment.
________________________________________
Team and Collaborators
•	Team ID: 5 
•	Team Members: Daneshwari, Chandana 
________________________________________
Prerequisites
To get started, make sure you have Python 3.8 or higher and pip (Python package installer) installed on your system.
________________________________________
Installation
1.	Clone the Repository
Start by cloning the project repository to your local machine using git.
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
2.	Create a Virtual Environment
It's highly recommended to use a virtual environment to manage dependencies for the project.
python -m venv venv
3.	Activate the Virtual Environment
o	On macOS and Linux:
source venv/bin/activate
o	On Windows:
venv\Scripts\activate
4.	Install Required Libraries
Install all the necessary Python packages using the command below.
pip install pandas scikit-learn numpy matplotlib seaborn joblib streamlit
These libraries are essential for data manipulation, model training, visualization, and creating the interactive GUI.
________________________________________
Usage
1. Data Preparation
The project is designed to work with a dataset of book reviews, specifically the all_kindle_review.csv dataset. The script can automatically detect and use a CSV file from a ZIP archive. The primary features used are reviewText (the full text of the review) and rating (the star rating). A binary popular target variable is engineered from the helpful column to classify reviews.
2. Running the Streamlit GUI
The easiest way to interact with this project is through the Streamlit application.
1.	Start the App:
From your terminal, with the virtual environment activated, run the Streamlit application.
streamlit run app.py
2.	Access the GUI:
Your web browser will automatically open the application at http://localhost:8501.
GUI Walkthrough
The Streamlit application provides a user-friendly interface for the entire machine learning pipeline .
•	Model Training & Evaluation:
o	Upload Data: Use the file uploader to select your .zip or .csv file.
o	Configure: Adjust the "Popular Rating Threshold" (e.g., a review is popular if its rating is 4 or higher) and the "Sample Size" to control the amount of data used for training.
o	Run: Click the "Start Training and Evaluation" button. The app will show a progress spinner and then display evaluation metrics, including accuracy, precision, recall, F1-score, and a confusion matrix for each trained model.
________________________________________
Methodology
The project follows a systematic machine learning methodology.
•	Data Preparation: The Kindle review dataset is loaded, and missing values are handled.
•	Feature Engineering: A binary popular target variable is created from the helpful column, and the reviewText is converted into numerical features using TF-IDF vectorization.
•	Model Training & Tuning: The data is split into training and testing sets. Various models, including Logistic Regression, LinearSVC, Random Forest, and Gradient Boosting, are trained and optimized using GridSearchCV.
•	Evaluation: Model performance is assessed using a standard set of metrics on the test set.
•	Interpretation & Saving: Feature importance is analyzed to identify influential words, and the final models and the TF-IDF vectorizer are saved to files for future use.
________________________________________
Results
The project successfully built a machine learning pipeline that can predict review popularity with high accuracy.
•	Key Finding: Logistic Regression and LinearSVC were the top performers, both achieving an accuracy of approximately 85%.
•	Linguistic Drivers: Feature analysis revealed that a review's sentiment and vocabulary are key to its popularity. Positive words (e.g., 'loved', 'wonderful') are strong predictors of popularity, while negative words (e.g., 'boring', 'disappointing') are strong indicators of an unpopular review.
•	Metrics: The Logistic Regression model achieved an accuracy of 85.2%, a precision and recall of 0.85, and an F1-Score of 0.85. A confusion matrix confirmed its robust performance24.

