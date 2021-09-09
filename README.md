"# Class task 1 "

There are 3 parts of the task 

1. Data scrapping using  beautifulsoup fromr web -02. Exploratory Data Analysis Data_creation.ipynb
2. 2nd part of the code is for ->03. Feature Engineering (Feature.ipynb )
3. part of the code is the Classification code SVM (Classfier.ipynb)


#Data Scappping  

In this notebook we'll do some exploratory data analysis over our dataset. 
we used followinng URLS to Scrap the data with 4 Category finance,technology, business,politics  for autnoumus car

"finance":["https://www.investopedia.com/articles/investing/052014/how-googles-selfdriving-car-will-change-everything.asp"]
"technology":["https://en.wikipedia.org/wiki/Self-driving_car","https://www.nhtsa.gov/technology-innovation/automated-vehicles-safety"]
"business":["https://www.wired.com/story/gm-driverless-toyota-e-palette-byton-ev"],
"politics":["https://www.latimes.com/politics/la-na-pol-self-driving-politics-20171121-story.html"] }

Data scrapping 

we have graphs  for 
1) Number of articles in each category Category.jpeg 
2) distribution  each category  distribution.jpeg ,distribution.jpeg 
3)box plot boxplot.jpec

we create  the car_dataset.pickle after screapping the data 

Feature Engineering
following steos were peeforme  

1)  Text cleaning and preparation
  special characters  removed  

	\r
	\n
	\ before possessive pronouns (government's = government\'s)
	\ before possessive pronouns 2 (Yukos' = Yukos\')
	" when quoting text
2 ) Converting all to lower case 
3 Punctuation signs   and  Possessive pronouns 	 removed 

4 ) Stemming and Lemmatization  were perodfmed \
5) Stop words were removed 

6) train /test was split  and hyper parmeter were set for classdier 
7) provide corelated features  the unigrams correspond well to their categoryas well bigrams do not.

8) files were saved in Pickel dir 
 following Pickle files were creates   for classifert

		df.pickle
		features_test.pickle
		features_train.pickle
		labels_test.pickle
		labels_train.pickle
		tfidf.pickle
		X_test.pickle
		X_train.pickle
		y_test.pickle
		y_train.pickle
		  

Classifier 


1) load the data from pickcle files 
2) setup Cross-Validation for Hyperparameter tuning including Randomized Search Cross Validation
3)SVm model is used for classfication 
4) best parameter  were found for examaple 
	The best hyperparameters from Random Search are:
	{'probability': True, 'kernel': 'poly', 'gamma': 10, 'degree': 4, 'C': 0.01}

		The mean accuracy of a model with these hyperparameters is:0.9212057112638815
		
5) Model fit  and run 
