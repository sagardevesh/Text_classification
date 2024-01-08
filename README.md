This project is part of the CSCI6409 Process of Data Science course. The project involves data preprocessing, exploratory data analysis, and building a text classification model using Multinomial Naive Bayes. The dataset used is sourced from a JSON file.

Here is the original [Amazon Books Reviews](https://www.kaggle.com/datasets/mohamedbakhet/amazon-books-reviews) dataset.

**Contributors:-**

Sagar Devesh

Sarthak Pandit 

## Project Structure
The project consists of three main sections:

### 1. Data Preprocessing
The initial steps involve importing relevant libraries, reading the JSON file, and performing basic data cleaning operations such as handling missing values and resetting the index. Additionally, downsampling the dataset to 10,000 rows is done for model training.

### 2. Textual Data Analysis
This section calculates various properties of the textual data, including text length, number of words, and the presence of non-alphanumeric characters. The data quality report for both categorical and continuous features is generated, providing insights into the dataset's statistical properties.

### 3. Text Classification Model
The Multinomial Naive Bayes algorithm is employed for text classification. The text is preprocessed by merging 'reviewText' and 'summary' columns, removing non-alphanumeric characters, and eliminating stop words. The model is evaluated using accuracy, ROC AUC score, and a learning curve.

### 4. Part of Speech Tagging and Model Comparison
In this optional section, part of speech tagging is performed on the merged text, and a new model is built using only nouns extracted from the text. The performance of both models is then compared using statistical significance tests.

### Additional Notes
The project utilizes various libraries such as pandas, numpy, nltk, and scikit-learn for data manipulation, analysis, and machine learning tasks.
Multinomial Naive Bayes is a naive bayes algorithm that assumes a multinomial distribution and is advantageous when the dataset is not too large. We have used 10000 samples for our modelling (which is not a huge number), hence we found multinomial Naive Bayes model to be appropriate. 
Evaluation metrics such as accuracy, ROC AUC score, and learning curves are presented for model assessment.
Part of speech tagging is performed to extract nouns, and a new model is built to observe its impact on performance.

## Steps to run on local machine/jupyter notebook:
To run this assignment on your local machine, you need the following software installed.

********************************************
Anaconda Environment

Python
*********************************************

To install Python, download it from the following link and install it on your local machine:

https://www.python.org/downloads/

To install Anaconda, download it from the following link and install it on your local machine:

https://www.anaconda.com/products/distribution

After installing the required software, clone the repo, and run the following command for opening the code in jupyter notebook.

jupyter notebook A3-Sagar_Devesh-Sarthak_Pandit.ipynb
This command will open up a browser window with jupyter notebook loading the project code.

You need to upload the dataset from the git repo to your jupyter notebook environment.


