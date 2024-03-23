## Aim:
To connect Amazon Managed Service for Apache Flink Studio to your existing stream, clean, aggregate, and enrich the incoming events, and derive insights finally persisted in Amazon OpenSearch, where they can be accessed and visualized.

### Step 1: Creating Stack from AWS CloudFormation
1. Go to AWS CloudFormation and click on create stack.
2. Click on Upload a template file and upload "kinesis-immersion-day-cfn.yaml" file.
3. Leave everything default and click on next.
4. Check all three boxes of acknowledgment and click on submit.
5. It will start creating all resources for you.

### Step 2: Creating Data Stream
1. Search Kinesis and click on Data streams.
2. Enter the name of your stream as "input-stream".
3. Click on create stream.

### Step 3: Generating Random Data
1. Search for AWS Cloud9 and click on auto-generated environment by AWS CloudFormation.
2. Upload the file named "Demo.py" from files in the top left corner.
3. In the terminal, install boto3 with the command: `pip install boto3`.
4. After installing boto3, run the Python script with the command: `python Demo.py`.
5. It will start generating random data for us to stream. You can go to your data stream and check activities under Monitoring.

### Step 4: Analyzing Streaming Data with AWS Kinesis Data Analytics for Apache Flink
1. Studio notebook will already be created by CloudFormation. Clicking on the studio notebook will take you to Zeppelin, which is an interactive data analytics and document collaboration notebook.
2. On the landing page of Zeppelin, upload KDA-OpenSearch.zpln file, and after uploading it, click it to view the notebook.
3. Update the host field with the OpenSearch domain endpoint copied from Amazon OpenSearch service.
4. Get the password from Secrets Manager as per the instructions provided and paste it in Zeppelin.
5. Execute the cells accordingly.

### Step 5: Visualization Process
1. Go to Amazon OpenSearch Service and click on the dashboard. Use the same admin name and password used in Zeppelin.
2. Select any tenants between global and private.
3. Run "select * from 'Name of your table' " to retrieve data.
4. Go to Stack management tab and select Index patterns. Create an index pattern with the same name as your index in step 3.
5. Now, go to visualize and create visualization of your choice.
