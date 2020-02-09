#### write commands for following mongodb opertaions

1. create a database named `sports`
   // Answer here ..

```js
  use sports
```

2. list all databases present in local mongod server.
   // Answer here..

```js
  show dbs
```

3. create 3 collections named `cricket`, `football`, `TT` in sports database.

```js
db.createCollection("cricket");
db.createCollection("football");
db.createCollection("TT");
```

4. add 3 players in each of above collections which should have fields like `name`, `age`, `email`, state and auction_price.

```js
db.cricket.insert({
	name: "virat",
	age: 31,
	email: "vkohli@gmail.com",
	auction_price: "17cr"
});
db.football.insert({
	name: "messi",
	age: 31,
	email: "lmessi@gmail.com",
	auction_price: "200cr"
});
db.TT.insert({
	name: "sharath",
	age: 37,
	email: "sharath@gmail.com",
	auction_price: "1cr"
});
```

5. list all collections in sports database.

```js
db.getCollectionNames();
```

6. rename `TT` collection to `tennis`.

```js
db.TT.renameCollection("tennis");
```

7. create a capped collection called `khokho` which should have max 3 documents.
   Try inserting more than 3 and output the result here ?

```js
db.createCollection("khokho", { capped: true, size: 2048, max: 3 });
```

8. check whether a collection is capped or not?

```js
db.khokho.isCapped();
```

9. remove all documents from `football` collection.

```js
db.football.remove({});
```

10. delete cricket collection completely.

```js
db.cricket.remove();
```

11. rename database sports to games

```js
db.copyDatabase("sports", "games");
```

12. delete sports database.

```js
use sports
db.dropDatabase()
```
