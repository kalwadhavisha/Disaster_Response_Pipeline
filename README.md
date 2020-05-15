# Disaster Response Pipeline Project

### Description:
This Project is part of Data Science Nanodegree Program by Udacity in collaboration with Figure Eight. The initial dataset contains pre-labelled tweet and messages from real-life disaster. The aim of the project is to build a Natural Language Processing (NLP) tool that categorize messages.

The Project is divided in the following Sections:

1. Data Processing, ETL Pipeline to extract data from source, clean data and save them in a proper databse structure
2. Machine Learning Pipeline to train a model able to classify text message in categories
3. Web App to show model results in real time.

### Content:
1. Data
    - process_data.py: reads in the data, cleans and stores it in a SQL database. 
       Basic usage is python process_data.py MESSAGES_DATA CATEGORIES_DATA NAME_FOR_DATABASE
    - disaster_categories.csv and disaster_messages.csv (dataset)
    - DisasterResponse.db: created database from transformed and cleaned data.
2. Models
    - train_classifier.py: includes the code necessary to load data, transform it using NLP,
       run a  machine learning model using GridSearchCV and train it. 
       Basic usage is python train_classifier.py DATABASE_DIRECTORY SAVENAME_FOR_MODEL
3. App
    - run.py: Flask app and the user interface used to predict results and display them.
    - templates: folder containing the html templates

### Dependencies:
1. Python 3.5+
2. Machine Learning Libraries: NumPy, SciPy, Pandas, Sciki-Learn
3. Natural Language Process Libraries: NLTK
4. SQLlite Database Libraqries: SQLalchemy
5. Model Loading and Saving Library: Pickle
6. Web App and Data Visualization: Flask, Plotly


### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/


### Licensing, Authors, Acknowledgements:
Credits must be given to Udacity for the course and the starter codes and FigureEight for provding the data used by this project.
