# Part 1

// importing the data in mongoDB database as amazon_db
mongoimport --db amazon_db --collection Electronics --type json --file '/home/cloudera/Downloads/Electronics_5.json'

//start mongoDB
mongo

//switch to this database
use amazon_db

// Showing only the summary and overall columns with overall rating 1,3, or 5.
db.Electronics.find({ 'overall': { $in: [1,3,5] } }, {'summary':1, 'overall':1, '_id':0} ).pretty()

// Showing only the reviewName and 'overall' columns with overall rating less than 3 (using $lt) and greater than 1 (using $gt) and sorting the result by the ascending alphabetic order of 'reviewerName'.
db.Electronics.find( { $and:[ {'overall':{$lt:3} }, {'overall':{$gt:1} } ] }, {'reviewerName':1, 'overall':1, '_id':0} ).sort( {'reviewerName':1} )

# Part 2

//Find the 'reviewText' that have the word 'awesome'.
db.Electronics.find({'reviewText':{$in:['awesome']}}).pretty()

//Find the 'summary' that have any characters apart form 'alphanumerical characters' and 'space'.
db.Electronics.find({'summary':{$regex:'[^a-zA-Z0-9 :]'}})

//Use $nin operator to show only the ‘summary’ and ‘overall’ columns where overall rating not in 2 and 4.
db.Electronics.find({'overall':{$nin:[2,4]}}, {'summary':1,'overall':1}).pretty()

//Show only the 'reviewerID' and 'reviewerName' column with the ascending order of 'reviewerID'. Show only first 10 result.
db.Electronics.find({}, {'reviewerID':1, 'reviewerName':1}).sort({'reviewerID':1}).limit(10) 

# Part 3

