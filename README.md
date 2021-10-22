# mongoDB_AmazonReviews
Manipulating Big Data using mongoDB.

Overview:

Download amazon video game review data from the link http://snap.stanford.edu/data/amazon/productGraph/categoryFiles/reviews_Electronics_5.json.gzLinks to an external site.. After extracting you will get a “.json” file. The description of the data can be found in the link http://jmcauley.ucsd.edu/data/amazon/Links to an external site.. For this assignment, you must run different queries on MongoDB using this dataset.

Point Distribution:

Part 1:

* Download and Insert this dataset to a MongoDB collection under a database.

* Use ‘OR’ operation to show only the ‘summary’ and ‘overall’ columns with overall rating 1 or 3 or 5.

* Use ‘AND’ operation to show only the ‘reviewerName’ and ‘overall’ columns with overall rating less than 3 (use $lt) and greater than 1 (use $gt) and sort the result by the ascending alphabetic order of ‘reviewerName’.

Part 2:

* Find the 'reviewText' that have the word 'awesome'.

* Find the 'summary' that have any characters apart form 'alphanumerical characters' and 'space'.

* Use $nin operator to show only the ‘summary’ and ‘overall’ columns where overall rating not in 2 and 4.

* Show only the 'reviewerID' and 'reviewerName' column with the ascending order of 'reviewerID'. Show only first 10 result.

Part 3:

* Group by ‘reviewerName’ to show the minimum ‘overall’ rating they posted. Show only 10 results.

* Group by ‘Helpful’ to show the ‘total number’ of entries found for different ‘Helpful’ data, sorted by descending order of the ‘total number’.

* Find the count of data where 'unixReviewTime' greater than a certain value (try different values of 'unixReviewTime' from the dataset to see if the result changes. Submit any of the result you got for your input value of 'unixReviewTime').

