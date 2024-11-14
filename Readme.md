# Project Overview

This repository contains a Python notebook for analyzing tweets related to the **Farmers' Protest 2021**.  The notebook performs pre-processing of the tweets and covers tasks such as **Exploratory Data Analysis**, **Entity Recognition**, **Index Construction**, and **Evaluation** of search performance.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Output](#output)
- [Index Construction and Evaluation](#index-construction-and-evaluation)
- [Scoring methods](#Scoring-methods)
- [Features](#features)
  

## Prerequisites

Ensure the following are installed on your machine:

- **Python 3.x**
- **Collab or Jupyter Notebook** or any Python-compatible IDE (such as VSCode or PyCharm)
- **Data Files**: Use this repository data folder to access all necessary data.
  - **farmers-protest-tweets.json.gz**: Contains raw tweet data. Note that we copressed the file due its large size.
  - **tweet_document_ids_map.csv**: Maps tweet IDs to document IDs.
  - **evaluation.csv**: ground truth file for queries 1 & 2.

## Usage

1. **Data Folder**:
   - Ensure all tweet data is stored in the `data/` folder, with appropriate file names matching the notebook paths.
   - The data should be in a structured format like CSV or JSON (or GZ if the data file is compressed).

2. **Notebook Execution**:
   - Open the `project.ipynb` notebook.
   - Execute the cells sequentially for preprocessing and exploratory data analysis, which include various tasks like entity recognition and word cloud generation.
   - Execute cells for building the search index, performing document retrieval based on queries, and evaluating performance metrics.

## Output

The notebook will generate:
- A pre-processed dataset where each tweet is cleaned, tokenized.
- Exploratory data visualizations such as word frequency distribution and hashtag analysis.
- A term-document index with TF-IDF weighting.
- Search results for predefined and custom queries.
- Evaluation metrics, including Precision, Recall, F1 Score, MAP, MRR, and NDCG.

## Index Construction and Evaluation

### Index Construction

The inverted index is built by processing each tweet, where:
- **TF** (Term Frequency) is computed as normalized term counts within each document.
- **DF** (Document Frequency) records the number of documents each term appears in.
- **IDF** (Inverse Document Frequency) is computed to adjust TF by penalizing terms common across many documents.

The index structure allows efficient search and retrieval of relevant tweets by terms.

### Query Execution

The following queries were defined to test the search engine:
- "Farmer protest"
- "Modi govt"
- "diesel price"
- "indian farmer"
- "Disha ravi"

### Evaluation Metrics

To evaluate the search engine’s performance, several metrics are implemented and calculated based on the ground truth labels:
- **Precision@k**: Measures the proportion of relevant documents in the top `k` retrieved documents.
- **Recall@k**: Measures the proportion of relevant documents retrieved out of all relevant documents for a query.
- **F1 Score**: Harmonic mean of Precision and Recall, providing a balance between the two.
- **Mean Average Precision (MAP)**: Average precision across queries, indicating search relevance consistency.
- **Mean Reciprocal Rank (MRR)**: Reciprocal of the rank of the first relevant document, averaged across queries, to measure responsiveness.
- **NDCG** (Normalized Discounted Cumulative Gain): A normalized ranking metric reflecting the quality of document ranking by relevance.

### Other scoring methods
Scoring Based on TF-IDF
Scoring Based on popularity
Scoring Based on BM25


### Key Results
The evaluation metrics provide insight into the search engine’s performance and guide improvements in the indexing or ranking algorithms.

## Features

- **Pre-processing**
- **Exploratory Data Analysis (EDA)**
- **Index Construction and Evaluation**
