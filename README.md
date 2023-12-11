# Creating Queries in Python in Files

In this lesson, we will generate queries from a datafile and obtain certain information about the data. The file that is being used is about nobel prize winners since the 1900s.

# Imports

```
import datetime
import numpy as np
import pandas as pd
```

To begin, let's read in the file that we are going to be using to generate the queries. Use the pd.read_csv() command for this because the data is a csv file. If the data file is another type of document, like a word document or an excel, use different commands, like the read_excel() command.

```
import pandas as pd
df = pd.read_csv('export.csv')
```
# Generating Queries
Let's generate some queries now that the file has been read in. The commands head() and tail() will generate either the first or last few items in the query. Let's generate the first 5 items in the set below:

Now, let's only view the category and years of the LAST 5 nobel prize winners:

```
df.tail(5)['year','category']
```

# loc[] command

Let's continue and generate another query, this time finding all males that have won a nobel prize in the query. In this instance, the loc[] command can be used to do this:

```
df.loc[df['gender'] == 'male']
```

We can expand on the loc[] command and generate another query, this time we can access all nobel prize winners from the current year, 2023:

```
df.loc[df['year'] == '2023', ['firstname','surname','category']]
```

# Your Turn

You can try some queries now, try writing queries to solve the following problems below:


Generate a query to find all nobel prize winners in the city "Munich":

```
df.loc[df['city'] == 'Munich']
```

Now, say that a company would like to send a letter to the hospitals where they were born. Write a query to find the birthday, birth city, and name of every nobel prize winner that is alive:

```
nobel[df.loc[df['died'] == '0000-00-00'], ['born','bornCity','name']]
```

Try and generate a query to find the first person to receive the nobel prize:
```

```

Finally, write a query to find all of the prize winners from France that won a nobel peace prize
```

```

# Conclusion
I hope that throughout this lesson in generating queries, you learned something new and that you are able to apply what you have learned to real world applications involving data science. I still have so much to learn, and everyone does so I hope that you take the time to learn new commands and expand your horizon.






