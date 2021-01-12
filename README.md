# data-tech-challenge
Hey Data Engineer. Welcome. Your mission, should you choose to accept it, is to analyse the following data and get back to us with the results.

## The Data

(see repository)

You are given a sample data dump (csv-format) comprising of ordered items of various orderbird customers. A row consists of 
* venue_id (string)
* item_name (string)
* datetime_ordered (string)
* turnover (double)
* invoice_id (string)

where 
* datetime_ordered denotes the timestamp when the item was ordered (bought)
* turnover (in EUR) is the price  
* invoice_id is an UUID of the associated invoice
  
Your task is to create some aggregations for a report for a German beverage company.
To this end, we ask you to create a jupyter/IPython notebook or python script in which you solve the tasks listed below. Popular tools for tackling such tasks are Pandas or pySpark. If you prefer another tool, please explain why. Finally, for a better understanding of your approaches and ideas, please comment your code.

## The Tasks:
# python 
1. Read data dump into a dataframe
2. What are the top 10 most ordered (bought) items in terms of item count?    
3. For each venue find
  3.1. the weekday on which the most items (in terms of item count) are ordered
  3.2. the item name which is ordered the most in terms of turnover
    
# docker 
1. Create docker image 
  1. for running a SQL database, e.g. postgres database
	2. initialized with the data dump 
2. Implement 3.1 and 3.2 in SQL
3. Demonstrate 
	1. how to start and access the docker image
	2. how to run queries from the command line 
  
# ETL design
Suppose you are asked to design an ETL process which daily delivers the aggregations to an industry partner as, e.g. a csv-file.
1. Please outline your design in the provided Miro-board.
2. We are very interested in your reasoning behind your design decisions. Please prepare yourself to explain them to us. 

# linux
Suppose a collegue of yours ran your python script for a bunch of days and stored stdout/stderr in a log-file, i.e *backfill_log.txt*. Unfortunetly, the script did not succeded for all days. Your task now is to
1. Demonstrate how to extract the dates for which the script failed by means of linux command line tools 
2. Compose an excecuteable .sh file consisting of all python commands for re-running the failed scripts where the usage of the script is as follows:
	python aggregate.py --date=YYYYMMDD

#
If you have any questions regarding these tasks, please just get in touch ( Tech-challenge@orderbird.com ) so we can clarify.


## And now what?
Please send your jupyter/IPython notebook or python script as well as your SQL-queries to Tech-challenge@orderbird.com and we will get back to you asap. 
Please *do not* create a pull request or fork this repository as your solution should not be end up being public afterwards.

Good luck and happy coding!


