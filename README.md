# VNExpress News Analysis Project

This project analyzes news articles from VNExpress to understand factors that influence the number of comments on articles and to classify articles between science and technology categories.

## Problem Statement

This project addresses two main tasks:

1. **Regression Task**: Predict the number of comments (`nums_of_comments`) on articles based on various features like title length, content, author, and publication time.

2. **Classification Task**: Classify articles into their respective groups (Science/Technology) based on textual content and metadata.

Based on initial data analysis, the regression task was selected as the primary focus due to interesting patterns observed between article characteristics and engagement metrics.

## Project Structure

vnexpress-analysis-project/ 
├── data/ 
│ ├── raw/ # Raw data files 
│ └── vnexpress_raw_data.csv
├── notebooks/ 
│ ├── 01_data_overview.ipynb 
│ ├── 02_data_cleaning.ipynb 
│ ├── 03_feature_engineering.ipynb 
│ ├── 04_data_visualization.ipynb 
│ └── 05_final_analysis.ipynb 
├── scripts/ 
│ ├── crawl_data.py 
│ ├── data_cleaning.py 
│ ├── feature_engineering.py 
│ └── visualization.py 
└── requirements.txt

