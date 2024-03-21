# TermPaper

Aim : To create datastream in AWS data stream and perform data visualization in AWS analytics


1) First we need to create stack from AWS CloudFormation -
   

i) Go to AWS CloudFormation and click on create stack

ii) Click on Upload a template file and upload "kinesis-immersion-day-cfn.yaml" file.

iii) Leave everything default and click on next.

iv) Check all three boxes of acknoledgement and click on submit.

Now it will start creating all resources for you

2) Now by the time it create all resources we will create data stream -


i) Search kinesis and click on Data streams

ii) Enter name of your stream as "input-stream"


3) After creating datastream, now we will go to Cloud9 for genrating random data for our stream -

i) Search for AWS Cloud9 and click on aouto genrated environment by AWS CloudFormation. 

ii) Upload file named "Demo.py" from files in top left corner.

iii) In terminal, now we will use boto3 which is used for integrate your Python application, library, or script with AWS services including Amazon S3, Amazon EC2, Amazon DynamoDB, etc. For this we wil use following command -
pip install boto3

iv) After installing boto3, we will run python script with following command-
python Demo.py

v) It will start genrating random data for us to stream. You can go to you data stream and check activities under Monitoring. Data will be visible to you in Monitoring tab after roughly 5-7 mins of starting program.

4) Now we will go to AWS kinesis and then go to Managed Apache Flink(AWS kinesis Data analytics) for analyzing straming data-


i) Studio notebook will be already been created by CloudFormation. When you will click on studio notebook, it will take you to Zeppelin which is interactive data analytics and document collaboration notebook. 
