# data-tech-challenge
Hey Data Engineer. Welcome. Your mission is to implement a data processing strategy which is relevant at orderbird. If you choose to accept the challenge then please let us know (data-tech-challenge@orderbird.com) how much time you would need to come back to us with your results. 

## The Data

(see repository)

You are given sample data files comprising of invoice data of various orderbird customers. 
A row consists of 

* venue_id (string)
* invoice_id (string)
* datetime_created (string)
* total (double)

where 

* venue_id is an unique outlet identifier
* invoice_id is a UUID of an invoice
* datetime_created denotes the timestamp when the invoice was created
* total is the invoice amout in EURO  

The date in a filename indicates that the invoice data was synced at that specific date to the backend system. It is important to notice, however, that an invoice could be created at **any** time in the past before the sync date!
  
## The Task:
Your task is to implement a strategy to efficiently update a table holding aggregated venues' totals. 
Technical requirements:

* the ETL-job is implemented in the Apache Airflow framework running inside a Docker container. 
* the ETL-job awaits a csv-file (in the format described above) in a mounted folder. 
* when a new data file is detected then its content is inserted into a RDS (running inside the Docker environment as well).

Here comes the challenging part:

* after successfully inserting the data then a second table holding aggregated total amounts per venue and per date of creation is updated.
* suppose that the invoice table was huuuuuge. Can you think of a non brute-force approach to **efficiently** update that aggregation table?

If you have any questions regarding these tasks, please just get in touch ( data-tech-challenge@orderbird.com ) so we can clarify.

## And now what?
Please send us a zipped file containing your docker project togther with instruction on how to use it.
Please *do not* create a pull request or fork this repository as your solution should not end up being public afterwards.

Good luck and happy coding!
