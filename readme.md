# Mongodb 

### what is mongodb :-
mongodb is nothing but a non-releational `(no-sql)` database management system that stores data in `documents(key-value)` format insted of `tables and rows`.
document is nothing but a collection of property

`Ex:-`
```
{
    name : 'Nikhil",
    age  :   21,
    city : 'solapur;
}
```

### Key Features:
- **Document-Oriented**: Data is stored in documents (similar to JSON), providing a more flexible schema than SQL databases.
- **Schema-less**: MongoDB allows you to store data without predefined schema, making it easier to handle dynamic data.
- **Scalability**: Supports horizontal scaling through sharding.
- **Indexing**: Supports indexing to improve query performance.
- **Replication**: Supports replication for high availability and data redundancy.
- **High Performance**: Optimized for high-performance data retrieval and storage.
- **Query Language**: Supports a query language similar to SQL, called MongoDB Query Language (MQL
- **Data Types**: Supports various data types, including strings, integers, dates, and more.
- **Aggregation Framework**: Supports an aggregation framework for complex data processing and analysis.
- **MapReduce**: Supports MapReduce for large-scale data processing and analysis.

### MongoDB Data Model
- **Documents**: The basic unit of data in MongoDB, similar to a row in a relational database
- **Collections**: A group of documents, similar to a table in a relational database
- **Databases**: A group of collections, similar to a schema in a relational database
- **Shards**: A group of collections that are distributed across multiple servers, used for horizontal scaling

### MongoDB Query Language (MQL)
- **Query Operators**: Used to filter data, such as `$eq`, `$ne`, `$gt
- **Query Methods**: Used to retrieve data, such as `find()`, `findOne()`,
- **Update Operators**: Used to update data, such as `$set`, `$inc`,
- **Delete Operators**: Used to delete data, such as `$pull`, `$pullAll`

### MongoDB Aggregation Framework
- **Pipeline**: A sequence of stages that process data, similar to a SQL query
- **Stages**: Individual steps in the pipeline, such as `match`, `group`, `
- **Operators**: Used to manipulate data, such as `$sum`, `$avg`, `$max`

### MongoDB MapReduce
- **Map Function**: Used to process data, similar to a SQL query
- **Reduce Function**: Used to aggregate data, similar to a SQL query


in sql we create a table in database.
but in mongodb we create collections.inside collection we create document(mentioned above)..

Ex:- `collections`

```
[
    {
        name : 'Nikhil",
        age  :   21,
        city : 'solapur;
    }
]
```

in sql database system. we use query language `(sql)` for intreacting.
but in mongodb database system we use `(mql)`=>(mongodb query language/mongodb api) for intreacting.



**COMMONDS**

1. To see how many databases are present in my system.

```
show dbs;
```


2. To create a new database / to switch to different db.

```
use database_name` (until and unless we dosent't create collection in database we can't see database)
```


3. To create a new collection

```
db.createCollection('collection_name')` => (`{ ok: 1 }`) means sucessfulley created collection in database.
```


4. To view the collection in a database

```
go inside database using `use database_name` and `show collection`
```


5. To create a new document/data/record

```
db.collection_name.insertOne({
    name: "Nikhil",
    age: 21,
    city: "Solapur"
});
```


6. To create multiple document/data/record we have to pass array of object.

```
db.collection_name.insertMany([
    {
        name: "Nikhil",
        age: 21,
        city: "Solapur"
    },
    {
        name: "Raj",
        age: 25,
        city: "Mumbai"
    },
    {
        name: "Sara",
        age: 22,
        city: "Pune"
    }
]);
```


7. To view data in a collection
```
`db.collection_name.find()`
```


8. To view data based on filter/condit(same like sql select,where)
```
db.collection_name.find({
    property: "value"
});
```


9. To update a one document/record/data
```
db.collection_name.updateOne(
    { property: "value" },   // Condition to match the document
    { $set: { property: "new_value" } } // Update operation
);
```


10. To update many document/record/data

```
db.collection_name.updateMany(
    { property: "value" },   // Condition to match multiple documents
    { $set: { property: "new_value" } } // Update operation
);
```


11. To delete record/document

```
db.collection_name.deleteOne({
    property: "value"
});
```


11. To delete many record/document

```
db.collection_name.deleteMany({
    property: "value"
});
```


12. To delete a collection (database and collection_name is there but complete document/record/data will be deleted)
```
db.collection_name.deleteMany({})`
```