# AIR-Semantic-Retrieval
Advanced Information Retrieval project using MiniLM for semantic search

## Project Title
Semantic Search for Amazon Product Reviews Using MiniLM

## Overview
This project investigates semantic information retrieval for Amazon product reviews.
A transformer-based dense retrieval model (MiniLM) is used to retrieve reviews relevant
to feature-oriented queries such as battery life, screen quality, and camera performance.

## Dataset
The dataset was provided as an HTML file containing Amazon product reviews.
Since the dataset did not include explicit numeric relevance labels, weak supervision
was applied for evaluation.

## Retrieval Models
- **MiniLM (Dense Retrieval)**  
  Reviews and queries are embedded using a pre-trained MiniLM model, and ranked using
  cosine similarity.

- **BM25 (Planned Baseline)**  
  A BM25 baseline was initially planned as described in the design document.
  However, after preprocessing the HTML dataset, the extracted review texts did not
  contain sufficient lexical tokens to compute stable BM25 statistics.
  Therefore, BM25 was excluded from the final experiments.

## Evaluation
Relevance labels were generated using keyword-based weak supervision.
The following metrics are reported:
- Precision@10
- Recall@10
- nDCG@10

## Project Structure
