1. Create a database named `blog`.

```
use blog
```

2. Create a collection called 'articles'.

```
db.createCollection("articles")
```

3. Insert multiple documents(at least 3) into articles. It should have fields

```js
db.articles.insertMany([
	{
		title: "learning MongoDB",
		description:
			"MongoDB is a No SQL database. It is an open-source, cross-platform, document-oriented database written in C++.",
		author: {
			name: "xyz",
			email: "abc@gmail.com",
			age: "30"
		},
		tags: ["js", "mongo"]
	},
	{
		title: "learning HTMl",
		description: "HTML and CSS...s",
		author: {
			name: "pqr",
			email: "abc@gmail.com",
			age: 25
		},
		tags: ["html", "css"]
	},
	{
		title: "learning Nodejs",
		description: "lorem Ipsum",
		author: {
			name: "abc",
			email: "abc@gmail.com",
			age: 23
		},
		tags: ["js", "web"]
	}
]);
```

4. Find all the articles using `db.COLLECTION_NAME.find()`

```
db.articles.find().pretty()
```

5. Find a document using \_id field.

```
db.articles.find({"id":ObjectId("5e3d0d549ea452ed0cd56b96") }).pretty()
```

6. Find documents using title and author's name field.

```
db.articles.find({title:"learning Nodejs", "author.name": "abc" }).pretty()
```

7. Find document using a specific tag.

```
db.createCollection("articles")
```

8. Update title of a document using its \_id field.

9. Update a author's name using article's title.

10. rename details field to description from articles collection.

11. Add additional tag in a specific document.

12. Update an article's tags using $set and without $set.

-   Write the differences here ?

13. Increment an auhtor's age by 5.

14. Delete a document using \_id field with `db.COLLECTION_NAME.remove()`.

Use sample.js data for below queries.

1. Find all males who play cricket.

2. Update user with extra golf field in sports array whose name is "Steve Ortega".

3. Find all users who play either 'football' or 'cricket'.

4. Find all users whose name includes 'ri' in their name.
