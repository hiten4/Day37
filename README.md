# Week 07 - NLP Assignment (ShopSense)

## Overview
This assignment focuses on implementing core NLP concepts including TF-IDF from scratch, similarity search, and evaluation against a standard library implementation. The goal is to understand how text representation works internally and how it can be applied to information retrieval tasks.

## Dataset
ShopSense E-Commerce Dataset:
- Reviews Dataset (~10,000 rows)
- Columns used:
  - review_text
  - category

## Tasks Completed

### Q1 - TF-IDF Implementation
- Implemented TF (Term Frequency) manually using word counts
- Computed IDF (Inverse Document Frequency) across the full corpus
- Built TF-IDF vectors without using sklearn
- Converted sparse dictionaries into vector form

### Query Matching
- Query: "wireless earbuds battery life poor"
- Converted query into TF-IDF vector
- Used cosine similarity to rank reviews
- Retrieved top 5 most relevant reviews

### Sklearn Comparison
- Used TfidfVectorizer from sklearn
- Compared results with custom TF-IDF
- Calculated average L2 distance between both matrices

### Word Importance Analysis
- Filtered reviews from Electronics category
- Computed average TF-IDF score for each word
- Identified the most important word based on score

## Q2 - Manual + Code Verification
- Calculated TF, IDF, and TF-IDF for the word "fabric" in a specific document
- Compared IDF values for:
  - Common word: "the"
  - Rare word: "embroidery"

### Key Insight
- Words like "the" appear in almost all documents → very low IDF
- Words like "embroidery" appear rarely → high IDF

## Why TF-IDF Instead of Frequency
Using only word frequency gives importance to common words that do not carry meaningful information. TF-IDF reduces the weight of such words and highlights terms that are more relevant to specific documents, making it more effective for search and ranking tasks.

## How to Run
1. Upload dataset to Google Colab:
   /content/shopsense_reviews.csv

2. Open the notebook:
   week07_nlp_assignment.ipynb

3. Run all cells in sequence

## Output
- TF-IDF matrix (custom implementation)
- Top 5 similar reviews for given query
- Average L2 difference vs sklearn
- Most important word in Electronics category
- TF, IDF, TF-IDF calculations for sample word

## Engineering Practices Followed
- Modular functions (TF, IDF, TF-IDF)
- Clear and readable variable naming
- Minimal hardcoding
- Basic error handling for missing data

## Conclusion
This assignment demonstrates how TF-IDF works internally and how it can be used for real-world tasks such as document ranking and keyword importance analysis. It also highlights the importance of validating custom implementations against standard libraries.
