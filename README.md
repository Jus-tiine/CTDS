
# Personalized News Recommendation System

This project aims to develop a personalized news recommendation system to enhance users' reading experience by aligning news suggestions with their interests and exploring popular trends. The project evaluates three approaches: frequent pattern-based, content-based, and reinforcement learning-based recommendations.

---

## Table of Contents
1. [Overview](#overview)
2. [Dataset](#dataset)
3. [Methods](#methods)
4. [Research Questions](#research-questions)
5. [Setup and Installation](#setup-and-installation)
6. [Usage](#usage)

---

## Overview
The exponential growth of online platforms has increased the need for effective filtering mechanisms to help users navigate the overwhelming amount of news articles. Personalized recommendation systems address this by suggesting relevant content based on user interests and behaviors.

This project evaluates the following approaches to recommendation:
- **Frequent Pattern-based Recommendations**: Identifies common patterns in article combinations using algorithms like A-Priori and PC-Y.
- **Content-based Recommendations**: Leverages text features from news articles using clustering methods and the BERT model.
- **Reinforcement Learning**: Applies DeepQ learning to dynamically adapt recommendations based on user feedback.

The project uses the [Microsoft News Dataset (MIND)](https://msnews.github.io/) as the foundation for data analysis and evaluation.

---

## Dataset
The Microsoft News Dataset (MIND) contains detailed logs of user interactions with approximately 160,000 English news articles. Key features of the dataset:
- **User Behavior Logs**: Includes interactions such as clicked and non-clicked events.
- **News Metadata**: Provides article details like title, abstract, category, and body.
- **Scale**: Includes data from over 1 million users, with a smaller subset of 50,000 users used for model training and evaluation. Due to limited computational resources, our work mostly used the MIND small dataset. However, each notebook will also run with the full dataset, provides enough resources are avaivible.

The dataset is divided into two primary files:
1. `behaviors.tsv`: Captures user click histories and impression logs.
2. `news.tsv`: Provides metadata for the news articles.

---

## Methods
The project implements and evaluates the following methods:

### Frequent Pattern-based Recommendation
- **Algorithms**: A-Priori, PC-Y
- **Goal**: Identify popular article combinations from user click histories.

### Content-based Recommendation
- **Clustering Methods**: Hierarchical Clustering, K-Means, DBSCAN
- **Feature Extraction**: BERT model for semantic analysis of articles.
- **Analysis Tools**: Elbow Method, Silhouette Analysis.

### Reinforcement Learning
- **DeepQ Learning**: Trains a model to adapt dynamically to user preferences for improved recommendations.

---

## Research Questions
This project addresses the following questions:
1. How can recommendations be made using frequent item pairs obtained from user histories?
2. How can recommendations be made by classifying feature groups of articles using clustering methods and BERT?
3. Can DeepQ Reinforcement Learning improve the quality of news recommendations?

---

## Setup and Installation
### Prerequisites
- Python 3.7+
- Required Python packages (listed in `requirements.txt`)

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/Jus-tiine/CTDS.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage
Download the [MIND dataset](https://msnews.github.io/) and place it in the `data/` directory.

Each Notebook is self contained as long all requirements and the above mentioned Dataset are set up correctly.
It is strongly recommended to run the Notebooks with the MIND small dataset initially, since the full set requires significant resources for BERT and DQR.

---
