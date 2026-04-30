# Data226 Homework 10 - Pinecone Airflow

This repository contains the files used for Homework 10: running a Pinecone job as an Airflow job.

## Files
- `docker-compose.yaml`
- `dags/build_pinecone_search.py`
- `HW10.pdf`

## Project Overview
This homework builds a Medium article search pipeline with Airflow and Pinecone.

The workflow includes:
1. Modifying `docker-compose.yaml` to install the required packages
2. Configuring Pinecone and creating an Airflow Variable for the API key
3. Downloading and preprocessing the Medium article dataset
4. Creating a Pinecone index
5. Generating sentence embeddings and ingesting vectors into Pinecone
6. Running a search query against Pinecone

## Airflow DAG
The DAG file is:

`dags/build_pinecone_search.py`

DAG name used in Airflow:

`Medium_to_Pinecone`

## Required Packages
The Docker Compose file includes:
- `sentence-transformers==3.1.1`
- `pinecone==5.3.1`

## Pinecone Configuration
An Airflow Variable was created for the Pinecone API key:

- `pinecone_api_key`

The Pinecone index name used by the DAG is:

- `semantic-search-fast`

## Report
The final report with screenshots and task logs is included as:

`HW10.pdf`
