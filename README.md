![Logo image](img/sbtscalasamlogo_small.png)

# sam-data-segment-seed.g8
A template project for quickly creating a serverless data-segment. A data-segment is a single element of a 
serverless data lake. When designed effectively, a grid of data-segments is effectively a data lake. A single data-segment
is designed as a [kappa-component](http://milinda.pathirage.org/kappa-architecture.com/). 
In the Kappa Architecture, the central storage mechanism is an append-only immutable log, here Kinesis. From the log, 
data is streamed through a computational system and fed into auxiliary stores for serving. A data-segment is made out
of a Kinesis Stream that is the immutable log, a Kinesis Extended S3 Firehose service and an S3 bucket that stores all 
log to an S3 bucket, effectively becoming a single element of the data lake. From the Kinesis Stream, computational 
components in the form of Kinesis Analytics will process data in real time.    

For more information see [sbt-sam](https://github.com/dnvriend/sbt-sam)

## Usage
Create a new template project by typing:

```
sbt new dnvriend/sam-data-segment-seed.g8
```

## Deploy
To deploy the project type `samDeploy`

## Remove
To remove the project type `samRemove`

## Info
To get deployment information like available endpoints and stack information, type `samInfo`

