# Stream Tweets and Put them to AWS Kinesis Data Streams

The flowchat of the project is showing as followings:

![image](https://user-images.githubusercontent.com/39544557/193456523-d9feed28-3259-4244-a8ec-3b4e1bef4339.png)


This project deals with how you can stream tweets using Twitter API v2 using Tweepy and insert them into a Kinesis Data Stream. This work is based on SUFIANKAKI/tweets2kinesis

While going through this project,I have upgraded the Twitter Developer to ELEVATED user.
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
