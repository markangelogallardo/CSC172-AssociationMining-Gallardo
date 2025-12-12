# CSC172 Association Rule Mining Project Proposal
**Student:** Mark Angelo L. Gallardo, 2022-0182  
**Date:** December 12, 2025
## 1. Project Title 
Bakery Sales Analysis using Apriori Algorithm


## 2. Problem Statement
Bakeries and Cafés face already experience high bread spoilage rates due to their short shelf life. To help with this and also increase profit, owners need to know not just what sells but also what sells with their offered product. This project analyzes transactional data to identify strong co-purchase patterns and check which have strong associations. Locally relevant for Philippine bakeries and cafes for analyzing customer buying behavior.

## 3. Objectives
- Preprocess the bakery/cafe data and perform EDA with visualizations
- Implement Apriori algorithm twice to generate association rules, one with coffee and one withour
- Evaluate rules using support, confidence, lift, and conviction metrics

## 4. Dataset Plan
- Source: Bread Basket Dataset - Kaggle (https://www.kaggle.com/datasets/mittalvasu95/the-bread-basket) (~9K transactions, 94 items)
- Domain: Bakery/Cafe transactions
- Acquisition: Direct Kaggle download to `data/bread_basket.csv`

## 5. Technical Approach
- Preprocessing: Handle missing values by dropping entires that have NULL values, use TransactionEncoder (from mlextend) to implement One-hot encoding
- Algorithm: Apriori (min_support=0.02, min_confidence=0.6, min_lift=1.2)
- Framework: Python + pandas + mlxtend + matplotlib/seaborn
- Environment: Jupyter Notebook / Google Colab

## 6. Expected Challenges & Mitigations
- Challenge: Sparse transaction matrix
- Solution: Filter infrequent items (support > 0.01)
  
- Challenge: Skewed to Coffee (likely most frequency item)
- Solution: Run the algorithm a second time, without coffee, to see other relationships past just Coffee
  
- Challenge: Trivial rules
- Solution: High lift threshold (>1.2)

