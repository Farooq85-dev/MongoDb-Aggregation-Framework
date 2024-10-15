# MongoDb-Aggregation-Framework

## This repository is about aggregation framework in MongoDb. What is aggregation pipelines? Happy Coding!

## Cursor Methods:-

### Most important cursor methods are below.

### 1) `sort`

#### It is used to sort the data in ascending or descending order. For example:-

```
db.mycollection.find().sort(username:1) // In Asc Order
db.mycollection.find().sort(username:-1) // In Desc Order
```

### 2) `limit`

#### It is used to limit the number of data. For example:-

```
db.mycollection.find().limit(1)
```

### 3) `skip`

#### It is used to skip number of provided documents. For example:-

```
db.mycollection.find().data(2)
```

### 4) `count`

#### It is used to count documents. For example:-

```
db.mycollection.find().count()
```

## Aggregation Framework

### Aggregation in MongoDB is a way to process documents in a collection by passing them through a pipeline of stages. Each stage performs an operation on the documents, such as filtering, sorting, grouping, reshaping, or modifying them. The results from each stage are passed to the next stage.

### `Situation #01:-`

#### Give me those users who name id 'farooq'. For example:-

```
[
  {
    $match: {
      name:'$farooq'
    }
  }
]
```

### `Situation #02:-`

#### Calculate all docs. For example:-

```
[
  {
    $count: 'All_Docs'

  }
]
```