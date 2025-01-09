# Data-Engineering-Project-Open-Source

Hi, thanks for stopping by! This space is where I document and practice building data engineering pipelines using open-source tools. I've learned so much from fellow engineers who generously shared their knowledge through documentation, GitHub, and YouTube videos. Now, it's my turn to give back to the community by creating detailed guides to help first-time engineers better understand the data engineering process. Here's my first data engineering project using open-source tools:

## Problem Statement

## Dataset

### My Laptop Specs**
- Macbook Air M1
- 512 GB Memory
- 8 GB RAM
  
## Setup Environment

### 1) MINIO
   -  Purpose: Object Store - to store raw, unstructured data
   -  Installation Guide: https://min.io/docs/minio/macos/index.html
   -  Helpful video: https://www.youtube.com/watch?v=sDICGMVldFk
   -  Start environement: terminal 'minio server start' 
   -  Access Web UI: http://127.0.0.1:9000
   
### 2) Docker
  - Purpose: Containerize packages
  - Installation: https://docs.docker.com/desktop/setup/install/mac-install/
  - https://stackoverflow.com/questions/44346109/how-to-easily-install-and-uninstall-docker-on-macos
    
### 4) Airflow
  - Purpose: Orchestration Tool
  - Installation: https://medium.com/orchestras-data-release-pipeline-blog/installing-and-configuring-apache-airflow-a-step-by-step-guide-5ff602c47a36
  - https://medium.com/@parklaus1078/airflow-installation-on-mac-811d60d7ed40
  - Access Web UI: http://localhost:8080
  - New Connection: Install Amazon connection package: pip install apache-airflow-providers-amazon
  - New Connection: Install Postgre connection package: https://airflow.apache.org/docs/apache-airflow-providers-postgres/stable/index.html
  - Start Web UI: airflow webserver -p 8080

## Airflow Configuration

  **1) Postgre Connection** 
     - Connection ID: postgres_default
     - Connection Type: Postgres
     - Local Host: localhost
     - Database: gold_layer
     - username: postgres
     - password: *** {need to setup in postgre}
     - 
   **2) Minio Connection**
      - Connection ID: aws_default
     - Connection Type: Amazon Web Services
     - Extra: {
                "aws_access_key_id": "minio_admin",
                "aws_secret_access_key": "minio_password",
                "endpoint_url": "http://host.docker.internal:9000"
              }
     
  4) Airbyte
    
### 5) Postgre
  - Install: https://www.enterprisedb.com/downloads/postgres-postgresql-downloads
  - Installation Guide: https://www.youtube.com/watch?v=PShGF_udSpk

## Methodology

### Step 1

### Step 2


## Troubleshooting:
- https://stackoverflow.com/questions/55729303/airflow-webserver-started-but-ui-doesnt-show-in-browser

- Check running airflow: sudo lsof -i tcp:8080
- Kill workflow : kill -9 {pid number}
