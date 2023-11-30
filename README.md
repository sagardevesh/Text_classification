This project is part of the CSCI6409 Process of Data Science course. The project involves data preprocessing, exploratory data analysis, and building a text classification model using Multinomial Naive Bayes. The dataset used is sourced from a JSON file ('sample1.jsonl').

Contributors
Sagar Devesh
Sarthak Pandit 

**Project Structure**
The project consists of three main sections:

1. Data Preprocessing
The initial steps involve importing relevant libraries, reading the JSON file, and performing basic data cleaning operations such as handling missing values and resetting the index. Additionally, downsampling the dataset to 10,000 rows is done for model training.

2. Textual Data Analysis
This section calculates various properties of the textual data, including text length, number of words, and the presence of non-alphanumeric characters. The data quality report for both categorical and continuous features is generated, providing insights into the dataset's statistical properties.

3. Text Classification Model
The Multinomial Naive Bayes algorithm is employed for text classification. The text is preprocessed by merging 'reviewText' and 'summary' columns, removing non-alphanumeric characters, and eliminating stop words. The model is evaluated using accuracy, ROC AUC score, and a learning curve.

4. Part of Speech Tagging and Model Comparison
In this optional section, part of speech tagging is performed on the merged text, and a new model is built using only nouns extracted from the text. The performance of both models is then compared using statistical significance tests.

Instructions for Running the Code
To reproduce the results, follow these steps:

Ensure you have the required dependencies installed. You can install them using:

bash
Copy code
pip install pandas numpy nltk scikit-learn matplotlib
Download the dataset ('sample1.jsonl') and place it in the project directory.

Run the provided Python script or Jupyter notebook for the assignment.

Additional Notes
The project utilizes various libraries such as pandas, numpy, nltk, and scikit-learn for data manipulation, analysis, and machine learning tasks.
The choice of using Multinomial Naive Bayes is explained in detail, and the hyperparameter tuning process is included.
Evaluation metrics such as accuracy, ROC AUC score, and learning curves are presented for model assessment.
Part of speech tagging is performed to extract nouns, and a new model is built to observe its impact on performance.
