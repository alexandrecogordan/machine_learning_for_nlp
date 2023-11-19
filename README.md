# Data Analysis and NLP

## Required Models/Resources

To run this project successfully, you'll need to download certain pre-trained models and resources. You can obtain them from the following links:

- **Wikipedia, PubMed, and PMC Word2Vec Model:**
  - [Download Link](http://evexdb.org/pmresources/vec-space-models/wikipedia-pubmed-and-PMC-w2v.bin)

- **BioWordVec PubMed and MIMIC-III Vector Model:**
  - [Download Link](https://ftp.ncbi.nlm.nih.gov/pub/lu/Suppl/BioSentVec/BioWordVec_PubMed_MIMICIII_d200.vec.bin)

Make sure to download and place these models in the appropriate directories (inside a models directory) before running the code. Refer to the documentation for instructions on how to incorporate them into the project.

## Project Overview

This repository is a comprehensive project that integrates data analysis with advanced natural language processing (NLP) techniques. Led by Alexandre Cogordan and Alexandre Brosseau, the project focuses on processing and analyzing textual data.

### Table of Contents

- [Data Analysis and NLP Project](#data-analysis-and-nlp-project)
  - [Overview](#overview)
  - [Contents](#contents)
  - [Usage](#usage)
  - [Dependencies](#dependencies)
  - [Notes](#notes)
- [Our Analysis](#our-analysis)
- [Creating Our Solution](#creating-our-solution)
  - [Pre-Processing](#pre-processing)
  - [Models](#models)
- [Evaluation of Our Factors Using a Graph](#evaluation-of-our-factors-using-a-graph)
  - [Chosen Factors](#chosen-factors)
- [Challenges & Explorations](#challenges--explorations)
  - [Challenges](#challenges)
  - [Explorations](#explorations)
- [Our Result](#our-result)

## Overview

This Jupyter notebook is a comprehensive project that merges data analysis with advanced natural language processing (NLP) techniques. The project focuses on the processing and analysis of textual data, with sections covering data preprocessing, model training (specifically Word2Vec and other embeddings), analysis and evaluation, and exploration of word embeddings.

### Contents

- **Data Preprocessing:** Implementation of text data preprocessing steps, including cleaning, tokenizing, and formatting.
- **Model Training:** Training of NLP models, with a specific emphasis on Word2Vec and potentially other embeddings (e.g., GloVe, BioWordVec).
- **Analysis and Evaluation:** Sections dedicated to the analysis of model outputs and performance evaluation.
- **Word Embedding Exploration:** Exploration of word embeddings to understand semantic relationships in text data.
- **Customizable Parameters:** Adjustable parameters for model training and analysis to suit different data sets and objectives.

### Usage

- Requires knowledge in Python, data analysis, and NLP.
- Designed to be executed sequentially: from data preprocessing to model training and analysis.
- Review each section for customization according to specific data and requirements.

### Dependencies

- Likely requires Python libraries such as gensim (for Word2Vec), nltk or similar (for text processing), and standard data science libraries like numpy, pandas.

### Notes

- The purpose and specifics of the text data and analysis objectives need to be defined by the user.
- Parameters and models should be adjusted based on the unique needs of the dataset and analysis.
- Ensure understanding of each code block before execution, especially in cases requiring custom data or setup.

## Our Analysis

We started by analyzing the provided corpus, gaining insights into queries and documents. The existing code was refactored for clarity, breaking it into functions for better understanding and efficiency.

## Creating Our Solution

### Pre-Processing

The pre-processing stage was enhanced with the implementation of the `clean_sentence` function, addressing noise removal, text standardization, lemmatization, and word length filtering.

### Models

Multiple models, including BM25, Word2Vec, GloVe, BioWordVec, and Wikipedia-Pubmed, were explored. We introduced a scoring function to weigh the influence of each model and experimented with different factors.

## Evaluation of Our Factors Using a Graph

We conducted evaluations to identify impactful factors and optimized their ranges for optimal scores.

### Chosen Factors

- Keeping the relevant documents: False
- Model’s vector size: 300
- Model’s vector window: 50
- Model’s minimum word count: 1
- Alpha value: 1
- Choice between cbow (sg = 0) or skip-gram (sg = 1): 0

## Challenges & Explorations

### Challenges

- Attempted improvements in pre-processing, including N-grams, led to worse scores.
- Limiting documents to the first 150 words resulted in a score drop.
- Summarization attempts were resource-intensive and impractical.

### Explorations

- Biobert or ClinicalBERT models could have been explored.
- Additional explorations like normalizing dates or handling medical acronyms were considered.

## Our Result

Based on the 150 first documents, we achieved an NDCG score of 0.912. Despite implemented solutions not directly improving scores, assumptions were made regarding vector usage. The project provides a satisfactory score for practical applications.

For detailed code implementation, refer to the [code repository](https://bit.ly/projet-nlp).

Here are some of the theses and resources that influenced our work:

- [SABER: A Visual Analysis System for Comparative Bio-Molecular Entity Recognition](https://baderlab.github.io/saber/resources/)
- [Article: Visual Analytics in Healthcare – Opportunities and Research Challenges](https://www.sciencedirect.com/science/article/pii/S2590177X19300563#b0245)
- [BioSentVec: Creating sentence embeddings for biomedical texts](https://github.com/ncbi-nlp/BioSentVec)

Feel free to explore these resources for a deeper understanding of the domain and methodologies applied in our project.
