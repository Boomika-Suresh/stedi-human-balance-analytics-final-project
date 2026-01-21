# stedi-human-balance-analytics-final-project
STEDI Human Balance Analytics

## Project Details
The STEDI Team has been hard at work developing a hardware STEDI Step Trainer that:

  * trains the user to do a STEDI balance exercise;
  * and has sensors on the device that collect data to train a machine-learning algorithm to detect steps;
  * has a companion mobile app that collects customer data and interacts with the device sensors.

STEDI has heard from millions of early adopters who are willing to purchase the STEDI Step Trainers and use them.

Several customers have already received their Step Trainers, installed the mobile application, and begun using them together to test their balance. The Step Trainer is just a motion sensor that records the distance of the object detected. The app uses a mobile phone accelerometer to detect motion in the X, Y, and Z directions.

The STEDI team wants to use the motion sensor data to train a machine learning model to detect steps accurately in real-time. Privacy will be a primary consideration in deciding what data can be used.

Some of the early adopters have agreed to share their data for research purposes. Only these customers’ Step Trainer and accelerometer data should be used in the training data for the machine learning model.

## Project Summary
As a data engineer on the STEDI Step Trainer team, you'll need to extract the data produced by the STEDI Step Trainer sensors and the mobile app, and curate them into a data lakehouse solution on AWS so that Data Scientists can train the learning model.

## AWS Environment
You'll use the data from the STEDI Step Trainer and mobile app to develop a lakehouse solution in the cloud that curates the data for the machine learning model using:

  * Python and Spark
  * AWS Glue
  * AWS Athena
  * AWS S3
    
## Data structure
STEDI has three JSON data sources(opens in a new tab) to use from the Step Trainer. Check out the JSON data in the following folders in the Github repo:
 * customer
 * step_trainer
 * accelerometer
Here are the steps to download the data:

1. Go to nd027-Data-Engineering-Data-Lakes-AWS-Exercises(opens in a new tab) repository and click on Download Zip.
2. Extract the zip file.
3. Navigate to the project/starter folder in the extracted output to find the JSON data files within three sub-folders. You should have
 * 956 rows in the customer_landing table,
 * 81273 rows in the accelerometer_landing table, and
 * 28680 rows in the step_trainer_landing table.

### Data preview
1. Customer Records
 * This is the data from fulfillment and the STEDI website.
 * Data Download URL(opens in a new tab) - AWS S3 Bucket URI - s3://cd0030bucket/customers/ contains the following fields:
   1. serialnumber
   2. sharewithpublicasofdate
   3. birthday
   4. registrationdate
   5. sharewithresearchasofdate
   6. customername
   7. email
   8. lastupdatedate
   9. phone
   10. sharewithfriendsasofdate

       
2. Step Trainer Records
 * This is the data from the motion sensor.
 * Data Download URL(opens in a new tab) - AWS S3 Bucket URI - s3://cd0030bucket/step_trainer/  contains the following fields:
   1. sensorReadingTime
   2. serialNumber
   3. distanceFromObject

      
3. Accelerometer Records
 * This is the data from the mobile app.
 * Data Download URL(opens in a new tab) - AWS S3 Bucket URI - s3://cd0030bucket/accelerometer/ contains the following fields:
   1. timeStamp
   2. user
   3. x
   4. y
   5. z
