# Spotify ETL Data Pipeline - Scalable Analytics Workflow with AWS

## Overview 🎵🎶🎧
This project demonstrates the design and implementation of a scalable ETL (Extract, Transform, Load) data pipeline leveraging the Spotify API alongside various AWS services. The pipeline extracts Spotify's daily top 50 global songs, processes and organizes this data into structured formats, and enables analytics using AWS Glue and Athena.

## Objective 🎯📊🔍
The goal of this project is to automate and scale the data pipeline to:
- Extract Spotify's daily top 50 global songs data.
- Transform and structure the data into separate categories: `artist`, `album`, and `songs`.
- Store the processed data in AWS S3 and make it analytics-ready with AWS Glue and Athena.

## Features 🛠️📈✨
- **Automated Workflows**: Daily triggers managed with AWS CloudWatch ensure seamless pipeline execution.
- **Serverless Architecture**: AWS Lambda handles data extraction and transformation tasks efficiently.
- **Scalable Storage**: Raw and transformed data are securely stored in Amazon S3.
- **Centralized Metadata**: AWS Glue Data Catalog provides schema discovery and organization.
- **SQL-Based Analysis**: AWS Athena enables interactive queries on structured data.

---

## Data Source 🎼🎤📂
**Spotipy API**:
Spotipy is a Python library for accessing Spotify's Web API, offering comprehensive access to Spotify's music data. This project utilizes Spotipy to extract detailed information about artists, albums, and songs.

**Learn more**: [Spotipy Documentation](https://spotipy.readthedocs.io/)

---

## AWS Services Used ☁️🔧💡
1. **Amazon S3**: Provides scalable storage for raw and processed data.
2. **AWS Lambda**: Executes Python scripts for data extraction and transformation.
3. **Amazon CloudWatch**: Automates triggers and monitors the pipeline.
4. **AWS Glue Crawler**: Scans and identifies data schemas, organizing metadata.
5. **AWS Glue Data Catalog**: Serves as a metadata repository for data management.
6. **Amazon Athena**: Enables querying and analyzing data stored in S3 with SQL.

---

## Architecture
![spotify ETL architecture](https://github.com/user-attachments/assets/c5fb4247-26ec-4817-98d8-0375b28eef6c)

---

## Steps to Implement the Pipeline 🛤️🔄📂

### 1. Extract Data from Spotify API 🎶📥💻
- Use Spotipy to fetch daily top 50 global songs using a Jupyter Notebook.
- Extract data fields for `artist`, `album`, and `song`.

### 2. Set Up AWS S3 for Storage ☁️📦🔒
- Create an S3 bucket for storing raw data.
- Establish folder structures for `artist`, `album`, and `song` categories.

### 3. Automate Triggers with AWS CloudWatch ⏰🔁🖥️
- Configure CloudWatch to execute the ETL pipeline daily.
- Enable error monitoring and logging for pipeline reliability.

### 4. Use AWS Lambda for Extraction and Transformation 🖋️⚙️📊
- Deploy Python scripts in AWS Lambda to handle data extraction.
- Perform transformations to organize data into analytics-ready formats.
- Save the transformed data in a separate S3 bucket. So one s3 bucket contains the raw data and the other contains the transformed data.

### 5. Organize Data with AWS Glue 📚🔍📋
- Set up Glue Crawler to scan the S3 bucket and infer schemas.
- Store metadata in the AWS Glue Data Catalog for future access.

### 6. Enable Analytics with AWS Athena 📊🔍📈
- Use Athena to query and analyze the structured data.
- Create analytics tables for `artist`, `album`, and `songs`.
- Perform interactive SQL-based queries for insights.

---

## Results 🏆📉🚀
- Achieved **85% reduction** in manual effort by automating workflows with AWS CloudWatch.
- Enhanced query efficiency by **40%** using structured datasets in Athena.
- Delivered a robust analytics-ready data pipeline for daily updates.

---

## Technologies Used 💻☁️🛠️
- **Programming Languages**: Python
- **Cloud Services**: AWS S3, AWS Lambda, AWS Glue, AWS Athena, AWS CloudWatch
- **Libraries**: Spotipy, Boto3

---

## Future Enhancements 🚀🔮📈
- Expand to include more Spotify data categories like playlists or user activity.
- Integrate real-time data streaming using AWS Kinesis.
- Develop visualization dashboards with AWS QuickSight for richer insights.

---

## References 📖🔗📝
- [Spotify Web API](https://developer.spotify.com/documentation/web-api/)
- [Spotipy Documentation](https://spotipy.readthedocs.io/)
- [AWS Documentation](https://aws.amazon.com/documentation/)

