#Class 2 Homework: Chiptole Data

##1. Look at the head and the tail of **chipotle.tsv** in the **data** subdirectory of this repo. Think for a minute about how the data is structured. What do you think each column means? What do you think each row means? Tell me! (If you're unsure, look at more of the file contents.)

The file is a list of every item from a series of chipotle orders, with the corresponding pricing. Each row is one item, not one order, and has one column for the protien and serving style options, and one column for all the additional ingredients. There is also a quantity of that item ordered and a final price. 

##2. How many orders do there appear to be?

There appear to be 1,834 total orders

code: `tail chiptole.tsv'

##3. How many lines are in this file?

using `wc -l chipotle.tsv`, I found there were 4,623 lines in the file

##4. Which burrito is more popular, steak or chicken?

Chicken burritos were ordered more often than steak burritos, so it seems Chicken is the more popular of the two burritos.

Code: `grep 'Chicken Burrito' chiptole.tsv' and `grep 'Steak Burrito' chiptole.tsv'

##5. Do chicken burritos more often have black beans or pinto beans?

Black beans are more popular for chicken burritos than pinto beans

Code: `'Chicken Burrito' chipotle.tsv | grep Black* | wc -l` and `grep 'Chicken Burrito' chipotle.tsv | grep Pinto* | wc -l`

##6. Make a list of all of the CSV or TSV files in the DAT8 repo (using a single command). Think about how wildcard characters can help you with this task.

I changed my working directory to the DAT-DC-10 folder and then used `find . -name *.*sv` to get the following list (git pull as of 12/6/15, AM):

```./data/airlines.csv
./data/bank-additional.csv
./data/bikeshare.csv
./data/chipotle.tsv
./data/drinks.csv
./data/hitters.csv
./data/imdb_1000.csv
./data/sms.tsv
./data/titanic.csv
./data/ufo.csv
./data/vehicles_test.csv
./data/vehicles_train.csv
./data/yelp.csv

```

##7. Count the approximate number of occurrences of the word "dictionary" (regardless of case) across all files in the DAT8 repo.

The word 'dictionary' appears in some form in 88 different locations across all files in the class repo. 
code: `grep -r 'dictionary' ~/Desktop/GA\ Data\ Sci/DAT-DC-10/ | wc -l` 

##8. **Optional:** Use the the command line to discover something "interesting" about the Chipotle data. Try using the commands from the "advanced" section!
