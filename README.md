# Stream Tweets and Put them to AWS Kinesis Data Streams

This work is based on SUFIANKAKI/tweets2kinesis

This work deals with how you can stream tweets using Twitter API v2 using Tweepy and insert them into a Kinesis Data Stream. The monitored keyword is "hashtag sports lang:en", to trace the twitter ID, TIMESTAMPS and Contents of the threads which is under "hashtag sports lang:en". 

![image](https://user-images.githubusercontent.com/39544557/193456523-d9feed28-3259-4244-a8ec-3b4e1bef4339.png)

I have followed the full instructions, here are the tips whilst doing this work:

While going through this work,I have upgraded the Twitter Developer to ELEVATED user.
![image](https://user-images.githubusercontent.com/39544557/193456404-1d0147c0-77e6-4e7d-96ab-630a291e444a.png)

From there, you should be inserting "tweetsbearertoken"

I have used ready-made script to get the Stream records `GetRecords.py`

I executed these scripts on an EC2 instance to which I attached an **IAM Role** allowing it to have the following permissions
Kinesis
- Write
  - Put Records
- Read
  - Get Records
  - Describe Stream
  - Get Shard Iterator
  
To reach S3 bucket will be create s3 bucket name and will go through Kinesis ingestion.
