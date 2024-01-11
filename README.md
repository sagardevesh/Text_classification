This project is part of the CSCI6409 Process of Data Science course. The project involves data preprocessing, exploratory data analysis, and building a text classification model using Multinomial Naive Bayes. The dataset used is sourced from a JSON file.

Here is the original [Amazon Books Reviews](https://www.kaggle.com/datasets/mohamedbakhet/amazon-books-reviews) dataset.

## Project Structure
The project consists of the following sections:

### 1. Data Preprocessing
The initial steps involve importing relevant libraries, reading the JSON file, and performing basic data cleaning operations such as handling missing values and resetting the index. Additionally, downsampling the dataset to 10,000 rows is done for model training.

Later on, as a part of preprocessing, we performed feature selection. We combined the review summary and text columns into one column called 'reviewTextSumaaryMerge'. After stop word removal, we used this column to get the tfidf vector and eventually feed it into the model.

### 2. Textual Data Analysis
This section calculates various properties of the textual data, including text length, number of words, and the presence of non-alphanumeric characters. The data quality report for both categorical and continuous features is generated, providing insights into the dataset's statistical properties.

Below is the continuous features report:-

![image](https://github.com/sagardevesh/Text_classification/assets/25725480/6ee0bbf0-3672-4409-8c81-a8fa3aec67e6)

Below is the categorical features report:-

![image](https://github.com/sagardevesh/Text_classification/assets/25725480/d00aff2b-dae2-4556-9c27-fff35258f534)

### 3. Text Classification Model
The Multinomial Naive Bayes algorithm is employed for text classification. The text is preprocessed by merging 'reviewText' and 'summary' columns, removing non-alphanumeric characters, and eliminating stop words. The model is evaluated using accuracy, ROC AUC score, and a learning curve.

Multinomial Naivev Bayes is a naive bayes algorithm that assumes a multinomial distribution and is advantageous when the dataset is not too large. Since we are using 10000 samples for our modelling, we found multinomial Naive Bayes model to be appropriate.

#### Avoiding Overfitting

To avoid overfitting in text classification, we can perform stemming and lemmatization of the data. In our case, we performed lemmatization. Lemmatization (and stemming) are ways to shrink the size of the vocabulary space.

For eg: By turning the words 'reading', 'reader' and 'reads' all into the stem or lemma 'read', the sparsity of the dataset can be drastically reduced. This really helps avoid overfitting because overly sparse data can lead to overfitting.

Stop word removal is also a step we performed that helps in avoiding overfitting. Stop words do not carry meaning of their own, but only in the context of a sentence. Having stop words can make the model more prone to overfitting. Therefore, preprocessing here plays a very important role to ensure that that the model does not overfit.

### 4. Part of Speech Tagging and Model Comparison
In this optional section, part of speech tagging is performed on the merged text, and a new multinomial Naive Bayes model is built using only nouns extracted from the text. The performance of both models is then compared using statistical significance tests.

### 5. Hperparameter Tuning
For hyperparameter tuning, we used HalvingRandomSearchCV for quicker results. The results showed that the model performs the best when the value of the parameter 'alpha' is 0.1 for Multinomial Naive Bayes.

### 6. Statistical Significance Test
Since we used the same model (Multinomial Naive Bayes) for both the scenarios, i.e before POS and after POS, the mean accuracy in both the instances was the same. This implies that part of speech tagging did not really have an impact on model's performance.

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


