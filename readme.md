# MongoDB CLI Reference Guide

**Start the Mongo CLI**

> `mongo`

---

**Show all DBs**

> `show dbs`

---

**Show current DB**

> `db`

---

**Switch to, and create if it doesn't exist, a DB**

> `use <name>`

---

**Clear the terminal page**

> `cls`

---

**Add to a collection**

> `db.collection-name.insert({ key : "value" })`

---

**See all collections within the current DB**

> `show collections`

---

**See all items within a given collection**

> `db.collection-name.find()`

_You can also pass an empty object {} inside the parentheses_

---

**See a list of items within a given collection, that match specific criteria**

> `db.collection-name.find({ key : "value" })`

_You can pass any criteria as a key to search by (ObjectID, "name", "completed")_

---

**Update an item in a collection**

> `db.collection-name.update({ Search-Key: "value" }, { To-Update-Key : "value to insert" })`

_If the item you're updating has any more keys/values than you set in this command, they will be erased_

---

**Update an item in a collection without removing other values**

> `db.collection-name.update({ Search-Key : "value" },{ \$set : { To-Update-Key : "value" }})`

---

**Delete all data within a collection**

> `db.table.remove({})`

_Note: The collection still exists_

---

**Remove a specific item from a collection**

> `db.collection-name.remove({ key : "value" })`

---

**Remove a collection from a DB**

> `db.collection-name.drop()`

_You don't have to remove data from the collection before you drop it. Returns "true" if it was successful. Optionally, you can include an empty object in the parentheses._

---

**Drop the currently in-use DB**

> `db.dropDatabase()`

_You should probably run 'db' to make sure you're using the correct DB first_
