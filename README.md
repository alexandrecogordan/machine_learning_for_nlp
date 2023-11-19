# NLP Project Readme

## Project Overview
This repository contains code and documentation for an NLP project focused on improving information retrieval using various models and techniques. The project is led by Alexandre Cogordan and Alexandre Brosseau.

### Table of Contents
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
