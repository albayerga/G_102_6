# Project Overview

This repository contains a Python notebook for analyzing tweets related to the **Farmers' Protest 2021**.  The notebook performs pre-processing of the tweets and covers tasks such as **Exploratory Data Analysis (EDA)**, **Entity Recognition**, **Word Cloud Generation**, and more.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Output](#output)
- [Features](#features)

## Prerequisites

Ensure the following are installed on your machine:

- **Python 3.x**
- **Collab or Jupyter Notebook** or any Python-compatible IDE (such as VSCode or PyCharm)
- **Data Files**: Place all data files in a folder named `data` within the project directory. The data is not included in this repository due to size limitations.
  - **farmers-protest-tweets.json**: Contains raw tweet data.
  - **tweet_document_ids_map.csv**: Maps tweet IDs to document IDs.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/albayerga/G_102_6.git
   cd G_102_6
   ```
   
2. **Install the required libraries**:
   If you encounter any missing dependencies during execution, install individual libraries as you go:
   ```bash
   python3 -m pip install <module_name>
   ```

   Or install directly inside a Jupyter notebook cell:
   ```python
   pip install <module_name>
   ```

3. **Run the notebook**:
   Open the notebook in Visual Studio Coder, Collab or your preferred IDE and execute the cells step by step.

## Usage

1. **Data Folder**:
   - Ensure all tweet data is stored in the `data/` folder, with appropriate file names matching the notebook paths.
   - The data should be in a structured format like CSV or JSON.

2. **Notebook Execution**:
   - Open the `part1.ipynb` notebook.
   - Execute the cells sequentially for preprocessing and exploratory data analysis, which include various tasks like entity recognition and word cloud generation.

## Output

The notebook will generate:
- A pre-processed dataset where each tweet is cleaned, tokenized.
- Exploratory data visualizations such as word frequency distribution and hashtag analysis.

## Features

- **Pre-processing**
- **Exploratory Data Analysis (EDA)**:
  - Word count distribution
  - Average sentence length
  - Vocabulary size
  - Word Cloud Generation
  - Entity Recognition
  - Top Retweeted Tweets
