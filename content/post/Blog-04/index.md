+++
title = "Feeling like a silly MONGO-ose"
date = 2019-08-06T20:06:21-07:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = []

# Tags and categories
# For example, use `tags =[]` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Mongo", "Mongodb", "R", "python"]
categories = []

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
# projects = [""internal-project""]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Center"
+++
Using Mongo/Mongod as a database <!--more-->


### Motivation for this post

I am currently working on a personal project where the database being used is MongoDB. Since this is my first time using it, I am going to record key commands and how I can to use it.


### The In-STALL-ling Process

[This](https://www.robinwieruch.de/mongodb-macos-setup/) resource was my saving grace to get started. I suggest following this walk through to Mongodb onto your system.


### Working with a `mongodb.tar.gz` file

I am using the open source [Open Food Facts database](https://world.openfoodfacts.org/data) for my project which means I downloaded this ~1.5GB file. Next I retreived the `.bson`  by unzipping the file and retreiving it from the `dump` folder.

in the bash terminal to start using the data from the mongodump this command was essential making sure you are located to wherever the `.bson` file is: 

```
mongorestore --db 'yourdbname' --collection 'yourcollectionname' name-of-file.bson
```

I did the following naming my database 'foodproducts` and my collection 'products'

```
mongorestore --db 'foodproducts' --collection 'products' name-of-file.bson`

```


In terminal, I made sure I was running both `mongod` and `mongo' with the respective commands

```
mongod
```

```
mongo
```

once in Mongo I was thrilled when I was able to access the data with 
```
use foodproducts
```

 and query using 
 
 ```
 db.products.find()
 ```
 
 This gave me access to the json formatted data and explore it. 
 
There is a lot of data in this database that is not useful for this particular project and I need to decrease the size of the file to be able to upload it to github and query it in a faster manner. 

To do this I decided to use an R package called `mongolite` this gave me the ability to 








