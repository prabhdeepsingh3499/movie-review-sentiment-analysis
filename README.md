# movie-review-sentiment-analysis

Analysis of Movie Reviews, classifying them as positive or negative using Machine Learning and Natural Language Processing.
### Summary
* Got a Movie Review Dataset from Kaggle
* Cleaned the Data by using NLTK, BeautifulSoup, regular expressions, string, and LabelEncoder libraries
* Split the training and testing data by 80/20 ratio
* Vectorized the reviews using TfidfVectorizer
* Built a model using Linear Support Vector Classifier
* Achieved 89% accuracy

### Data Collection
* Link to dataset: https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews
1. Understanding the dataset
* Let's read the context of the dataset to understand the problem statement. 
2. Downloading the dataset 
* Now that you have an understanding of the dataset, go ahead and download the CSV file. Simply click "Download (63MB)."
### Exploratory Data Analysis
* Let's check what the data looks like
![Description of Data](https://github.com/prabhdeepsingh3499/movie-review-sentiment-analysis/blob/master/img/EDA.png?raw=True)
* Notice how the data contains HTML tags and special characters. We will clean them in the data cleaning step.
* Check if there was any missing value. There was no missing value.
![Missing Values](https://github.com/prabhdeepsingh3499/movie-review-sentiment-analysis/blob/master/img/NullValues.png?raw=True)
### Data Cleaning
* First we convert the reviews into lower case
* By using Beautiful Soup we will remove the HTML tags found in our reviews
* By using NLTK library we tokenize the text, remove stopwords, lemmatize the text i.e convert it into its root form
* By using string library we remove the punctuations in the reviews
* By using regular expressions library we remove special characters and numbers found in our reviews
* By using LabelEncoder we encode our sentiment column as it is categorical and algorithms will not work for categorical data. 1 represents a positive sentiment and 0 represents a negative sentiment
* After that we assign sentiment column as y variable and review column as X variable
![Cleaned Data](https://github.com/prabhdeepsingh3499/movie-review-sentiment-analysis/blob/master/img/CleanText.png?raw=True)
### Train Test Split
* Now that we have cleaned our data, we will do train and test split using train_test_split function
* We will use 80% of data as training data and 20% of data as testing data.
### Vectorize reviews with TfidfVectorizer
* Now, we will convert text into numeric form as our model won't be able to understand the human language. We will vectorize the reviews using TfidfVectorizer. TfidfVectorizer is used to convert a collection of raw documents into a matrix of TF-IDF features.
### Model Building
* Now that we have vectorized all the reviews, we will build a model to classify the test data. 
* We will use a supervised learning algorithm, Linear Support Vector Classifier (LSVC). It is widely used for binary classifications and multi-class classifications.
* You can find more explanation on scikit learn documentation page-https://scikit-learn.org/stable/modules/generated/sklearn.svm.LinearSVC.html
### Accuracy
* The accuracy turned out to be 89%!
![Accuracy & Classification Report](https://github.com/prabhdeepsingh3499/movie-review-sentiment-analysis/blob/master/img/Accuracy.png?raw=True)
