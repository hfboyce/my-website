+++
title = "A Post about Python and R, post being in Postgres"
date = 2019-07-20T20:06:21-07:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = []

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Postgres", "python", "R"]
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
  caption = "[source](https://www.dummies.com/education/math/statistics/how-to-determine-a-p-value-when-testing-a-null-hypothesis/)"

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = " "
+++
  How to bring in a Postgres database into Python and R. <!--more-->
     
### Motivation for this post?

I recently explored data that was stored using Postgres. Because time was limited for this particular project and because I enjoy finding and vusualizing insights simultaneously, I wanted to do my queries directly in the language I would be conducting EDA. 

Finding that there were limited resources that explained this process, I thought I would inform others of the way that I went about it. 

{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
library(RPostgreSQL)
library(RPostgres)
library(tidyverse)

{r }
drv <- dbDriver("PostgreSQL")
dbListConnections(drv)
dbGetInfo(drv)

con <- dbConnect(RPostgres::Postgres()
     , host='localhost'
     , port='5432'
     , dbname='freshprep'
     , user='hayleyboyce')


dbListTables(con)
length(dbListTables(con))

dbExistsTable(con, "skips")

{r}
data <- dbReadTable(con, "billing_charges")
#data %>% filter(failure_reason != "NONE")
data

```import psycopg2 as pg
import sys, os
import numpy as np
import pandas as pd
import pandas.io.sql as psql```
```connection = pg.connect("dbname=freshprep user=hayleyboyce")```
```cursor = connection.cursor()
cursor.execute("select relname from pg_class where relkind='r' and relname !~ '^(pg_|sql_)';")
table_names = cursor.fetchall()
for i in table_names:
    print(i[0])```

```dataframe = psql.read_sql("SELECT * FROM orders", connection)```
```dataframe[dataframe["client_id"] == 401]```




