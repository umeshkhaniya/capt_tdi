# Solar Market Analysis in New York City And Albany
This project involves the potential location for solar market in New York City And Albany based on zip code. The datas used in the project are from solar radiation dataset and photovoltic rooftop data set. The data used here is from year 2013 since we only have common data for both set for year 2013. This project will accurately predict the potential location for solar industry.

# Introduction: 
Solar power is a clean and  renewable source of energy. As the world is moving to clean energy, the urban solar market has a great future in the world.
Therefore, analyzing the solar power market  is very important for solar industries. By keeping in mind, this project is investigaing the zip code location for  solar panel market.

# Data Source 
- Solar radiation data for year 2013: 1.6 TB
- PhotoValtic Data Source for year 2013: 6 GB

# ETL Pipleline
- Used the Pyspark for analysis data in aws EMR cluster.

# Bootstrapping Script
The software and dependencies requiremnts can be found in bootstrap_cap.sh file
 sudo python3 -m pip install \
  awscli \
 boto3 \
 ec2-metadata \
 s3fs \
 cython \
 h5py \
 pygeohash \
 shapely \
 uszipcode

# Scripts
The jupyter notebook is provided here is used  in running  EMR cluster to setup the system.
Python Script can directly used to run in the EC2 instance.
1. Creating the S3 bucket, EMR cluster using boto3: aws_system_preparation.ipynb
2. Processing the 1.6 TB data using the partition in EMR jupyter Notebook. This will save the data in local S3 bucket.
3. Processing Photovoltic data using EMR jupyter Notebook and saved into local S3 bucket.
4. This will join the two data using the Geohash and final data is stored in S3 bucket for analysis.
5. Small sample of data is loaded into s3 bucket and use the visualization. 
6. Heroku is used for deployement of data.
# Frond end website on Heroku
Link: 

