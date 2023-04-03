# mongoDBcheetsheet

Basics:

mongo: Opens the MongoDB shell.
show dbs: Lists all the databases on the server.
use <database>: Switches to a specific database or creates a new one.
db: Shows the current database.
db.dropDatabase(): Drops the current database.
db.<collection>.count(): Returns the number of documents in the collection.
db.<collection>.distinct(<field>): Returns an array of distinct values for the specified field in the collection.
db.<collection>.stats(): Returns statistics about the collection, such as the number of documents, the size of the collection, and the amount of disk space used.

Collections:

db.createCollection(<name>, <options>): Creates a new collection with the specified name and options.
db.<collection>.insert(<document>, <options>): Inserts a new document into the collection with the specified options.
db.<collection>.insertMany(<documents>, <options>): Inserts multiple documents into the collection with the specified options.
db.<collection>.find(): Returns all documents in the collection.
db.<collection>.find(<query>, <projection>): Returns documents that match the specified query and projection.
db.<collection>.findOne(<query>, <projection>): Returns the first document that matches the specified query and projection.
db.<collection>.update(<query>, <update>, <options>): Updates documents that match the specified query with the specified update and options.
db.<collection>.updateMany(<query>, <update>, <options>): Updates multiple documents that match the specified query with the specified update and options.
db.<collection>.replaceOne(<query>, <replacement>, <options>): Replaces a single document that matches the specified query with the specified replacement and options.
db.<collection>.deleteOne(<query>, <options>): Removes a single document that matches the specified query with the specified options.
db.<collection>.deleteMany(<query>, <options>): Removes multiple documents that match the specified query with the specified options.

Query Operators:

$and: Joins query clauses with a logical AND and returns all documents that match the conditions.
$or: Joins query clauses with a logical OR and returns all documents that match the conditions.
$not: Inverts the effect of a query expression and returns all documents that do not match the expression.
$nor: Joins query clauses with a logical NOR and returns all documents that fail to match both conditions.
$exists: Matches documents that have the specified field.
$type: Matches documents that have the specified data type for the specified field.
$mod: Performs a modulo operation on the specified field value and returns documents that match the result.
$regex: Matches documents that match the specified regular expression pattern.
$text: Performs a text search on the specified field and returns documents that match the search query.
$where: Matches documents that satisfy the JavaScript expression.

Aggregation:

$project: Reshapes each document in the collection by adding, renaming, or removing fields.
$match: Filters documents by a specified condition.
$limit: Limits the number of documents returned.
$skip: Skips a specified number of documents and returns the rest.
$sort: Sorts documents based on a specified field or fields.
$group: Groups documents by a specified field and performs aggregate functions on the groups.
$unwind: Deconstructs an array field from the input documents and outputs one document for each element.
