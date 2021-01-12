# data-tech-challenge
Hey Data Engineer. Welcome. Your mission, should you choose to accept it is to analyse the following data and get back to us with the results.

## The Data

(see repository)

You are given a sample data dump (csv-format) comprising of ordered items of various orderbird customers. A row consists of 
* venue_id (string)
* item_name (string)
* datetime_ordered (string)
* turnover (double)
* invoice_id (string)

where 
* datetime_ordered denotes the timestamp when the item was ordered
* turnover (in EUR) is the price  
* invoice_id is an UUID of the associated invoice

As you will see, the item names do not follow any conventions, could be misspelled or even abbreviated. 
  
Your task is to create some aggregations for a report for a German beverage company.
To this end, we ask you to create a jupyter/IPython notebook or python script in which you solve the tasks listed below. Popular tools for tackling such tasks are Pandas or pySpark. If you prefer another tool, please explain why. Finally, for a better understanding of your approaches and ideas, please comment your code.

## The Tasks:

1. Read data dump
2. What are the top 10 most ordered items in terms of item count?    
3. For each venue find
 
    3.1. the weekday on which the most items (in terms of item count) are ordered
     
    3.2. the item name which is ordered the most in terms of turnover
    
4. docker: 
  4.1 Create docker image with a running postgres and initialized with the data dump 
  4.2 Implement 3.1 and 3.2 as SQL queries
  
5. Miro and ETL design
Suppose you are asked to design an ETL process which daily delivers the aggregation to an industry partner as a csv-file.
5.1 Please outline your design in the provided Miro-board.
5.2 Make sure you can explain the reasoning behaind your design decisions.

6. Linux
Suppose you ran a backfilling process ...


If you have any questions regarding these tasks, please just get in touch ( Tech-challenge@orderbird.com ) so we can clarify.

### Hint
Regarding task no 1. : please do not aim for 100% accuracy here, since this can be a real time-sucker :-) . Start with a "good enough" solution first and describe future improvements without implementing these.

## And now what?
Please send your jupyter/IPython notebook to Tech-challenge@orderbird.com and we will get back to you asap. 
Please *do not* create a pull request or fork this repository as your solution should not be end up being public afterwards.

Good luck and happy coding!


