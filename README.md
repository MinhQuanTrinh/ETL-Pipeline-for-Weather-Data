# ETL Pipeline for Weather Data of Perth
Simple AWS ETL Pipeline for data from OpenWeather API

This project aims to display my capability of creating a simple ETL Data Pipeline from Scratch. The Components of this Pipeline are:
  1. OpenWeather API
  2. AWS EC2
  3. VSCode with SSH connection to EC2 instance
  4. AWS S3 as the destination of data
  5. Apache Airflow for Orchestration

This pipeline is based on the tutorial video https://www.youtube.com/watch?v=uhQ54Dgp6To&list=PLWB43E_5NBT-f2Wlab5wdaPiENe3m-gFz&index=4.
There are some changes in Airflow setup as the versions for Ubuntu are different. The maincode weather_dag.py is located: /airflow/dags/weather_dag.py

Apache Airflow orchestrates the following:
The API from OpenWeather is used to collect weather data of Perth (WA).
The data is transformed using Pandas and converted to csv.
The csv file is then loaded into AWS S3 Bucket.

#28/01/2025:
- Issue with installing awscli: E: Package 'awscli' has no installation candidate --> result in csv file cannot be loaded into S3 but saved in
the working directory.
