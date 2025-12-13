# CSC172 Association Rule Mining Project Progress Report
**Student:** Mark Angelo L. Gallardo, 2022-0182  
**Date:** December 13, 2025  
**Repository:** https://github.com/markangelogallardo/CSC172-AssociationMining-Gallardo

## 📊 Current Status
| Milestone | Status | Notes |
|-----------|--------|-------|
| Dataset Preparation | ✅ Completed | 9,465 transactions processed |
| Data Preprocessing | ✅ In Progress | One-hot encoded matrix not yet ready, data_time column expanded for temporal analysis|
| EDA & Visualization | ✅ In Progress | Temporal Analysis done, Item frequencies done, basket sizes to be done tomorrow |
| Apriori Implementation | ⏳ Pending | Initial run tomorrow |
| Rule Evaluation | ⏳ Not Started | Planned for next day |


## 1. Dataset Progress
- **Total transactions:** 9,465
- **Unique items:** 94 <!-- → filtered to top 30 (support > 0.01) -->
- **Matrix size:** 9,465 transactions × <!-- 30 items (2.1% density) -->
- **Column Expansion** date_time -> date, time, month, hour, day_of_the_week
- **Preprocessing applied:** <!-- one-hot encoding , infrequent item filtering, --> column expansion  

**Sample transaction preview:**  
Transaction 1: ['Bread']  
Transaction 2: ['Scandinavian', 'Scandinavian']

## SECTION BELOW IS FROM GIVEN FORMAT

## 2. EDA Progress

**Key Findings (so far):**
![Item Frequency Distribution](results/item_frequencies.png)
- Top 5 items: whole milk(25.3%), other vegetables(19.1%), rolls/buns(17.4%)
- Average basket size: 2.4 items
- 68% transactions contain 1-3 items

**Current Metrics:**
| Metric | Value |
|--------|-------|
| Transactions cleaned | 9,708/9,835 (98.7%) |
| Sparsity reduced | 0.12% → 2.1% |
| Top item support | whole milk: 0.253 |

## 3. Challenges Encountered & Solutions
| Issue | Status | Resolution |
|-------|--------|------------|
| High matrix sparsity | ✅ Fixed | Filtered to top 50 items |
| Memory usage (1.2GB) | ✅ Fixed | Sparse matrix format |
| Infrequent items | ⏳ Ongoing | Tuning min_support threshold |

## 4. Next Steps (Before Final Submission)
- [ ] Complete co-occurrence heatmap
- [ ] Run initial Apriori (min_support=0.02)
- [ ] Generate top 25 rules with metrics
- [ ] Create rule scatter plot 
- [ ] Record 5-min demo video
- [ ] Write complete README.md 