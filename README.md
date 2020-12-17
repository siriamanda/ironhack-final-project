# ironhack-final-project

## Background

Sentiment analysis is a Natural Language Processing technique concerned with detecting favourable and unfavourable opinions in textual data. It can be used to answer questions about people’s feeling towards a certain topic.

Due to the large volumes of textual data produced on the Internet, sentiment analysis has lately been included in the research toolbox of many companies as a way to find out what customers think about their product and organisation. 

There are two major approaches to sentiment analysis: 

- Rule based: in which a dictionary is used for automatic classification of sentiment 
- Feature based: in which machine learning models are trained based on labelled data

In this project I have tried both approaches but focused on a machine learning approach using Naive Bayes Classification. 

I wanted to explore the use of sentiment analysis in organisations and how sentiment analysis can be used for analysing reviews.

### Hypothesis

HO: Naive Bayes Classification is not a good method for analysing customer reviews

HA: Naive Bayes Classification is a good method for analysing customer reviews

## Data

Data source 1: Kaggle E-Commerce clothing reviews

https://www.kaggle.com/nicapotato/womens-ecommerce-clothing-reviews

Data source 2: Trustpilot reviews

Used web-scraping to extract customer reviews from three fashion E-Commerce organisations on Trustpilot.

# Content

1-web-scraping-trustpilot (notebooks and scraped datasets)

2-data-cleaning-preprocessing (notebooks and datasets)

3-modelling (notebooks and datasets)

4-Sentiment-analysis-using-Textblob (notebooks and dataset)

5-presentation (presentation slides)

## Workflow

### 1. Webscraping

Extracted 48,000 customer reviews from Trustpilot using BeautifulSoup. Saved dataframes in three csv files. 

### 2. Data exploration/cleaning

- Visualisations (G Ranjith kumar (2020), Shirell da Villa (2019))
- Drop null values
- Convert reviews to lowercase
- Remove: Stopwords, punctuations and numbers

### 3. Preprocessing 

- Tokenization
- Part of speech tagging
- Lemmatization

(Kamil Mysiak (2019) and Rachel Koenig (2019))

### 4. Modelling

Creation of a balanced sample by taking a random sample from each class and concatenating in a dataframe. 
Confirming representativeness with inferential statistics (Z-test). 

Train/test split.

Creation of the model pipeline:

- CountVectorizer
- TFID-Transformer
- MultinomialNB()

Suyash Pratap Singh (2020)

Model comparison: LogisticRegression(), DecisionTreeClassifier(), RandomForestClassifier() and svm.SVC()

### 5. Textblob analysis

Basic polarity analysis using textblob.


## Conclusion

While Naive Bayes prove to be able to predict sentiment of labelled data sources when the dataset is balanced, I do not have enough evidence to reject the null hypothesis. Naive Bayes is only useful for analysing sentiment in annotated datasources, and therefore Textblob or other rule-based approach would provide more valuable insights when analysing customer reviews.

## Future focus

Balancing data using oversampling techniques. Finetuning the model.


## Resources

MonkeyLearn (2020) https://monkeylearn.com/sentiment-analysis/

Ryan Cranfill (2016) https://ryan-cranfill.github.io/sentiment-pipeline-sklearn-2/

Code for visualisations:

G Ranjith kumar (2020) https://www.kaggle.com/granjithkumar/nlp-with-women-clothing-reviews

Shirell da Villa (2019) https://www.kaggle.com/shirellamosi/sentiment-analysis-nlp

Code for preprocessing:

Kamil Mysiak (2019) https://towardsdatascience.com/preprocessing-text-data-using-python-576206753c28

Rachel Koenig (2019) https://towardsdatascience.com/nlp-for-beginners-cleaning-preprocessing-text-data-ae8e306bef0f

Code for model pipeline:

Suyash Pratap Singh (2020) https://www.kaggle.com/suyashpratapsingh/eda-and-sentiment-analysis








