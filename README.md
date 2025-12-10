
# Market Basket Analysis - Algorithms for Massive Data

**Author:** Lejda Kolaveri  
**Course:** Algorithms for Massive Data (2024/2025)  
**Dataset:** [Amazon Books Reviews (Kaggle)](https://www.kaggle.com/datasets/mohamedbakhet/amazon-books-reviews)

---

## Project Overview
This project implements **Frequent Itemset Mining** techniques on a large-scale dataset of Amazon Book Reviews (~3 million rows). The goal is to uncover latent patterns in textual content and user purchasing behavior using distributed computing paradigms.

The project is divided into two tasks:

### 🔹 Task A: Words as Items (Text Analysis)
*   **Goal:** Find frequent word associations and linguistic patterns in review texts.
*   **Algorithm:** **SON Algorithm** (Savasere, Omiecinski, and Navathe).
*   **Implementation:** Two-phase MapReduce (Local Candidate Generation $\to$ Global Validation).
*   **Key Finding:** Identified strong linguistic collocations (e.g., `highly` $\to$ `recommend`) and sentiment markers.

### 🔹 Task B: Books as Items (User Behavior)
*   **Goal:** Identify books frequently reviewed together by the same user.
*   **Algorithm:** **Multistage Algorithm** (an extension of PCY).
*   **Implementation:** Iterative Hashing with Bloom Filters (Bitmaps) to handle memory constraints.
*   **Key Finding:** Detected clusters of classic literature (e.g., Jane Austen, Brontë sisters) and edition redundancies.

---

## Technologies & Scalability
*   **Language:** Python 3
*   **Framework:** Apache Spark (PySpark)
*   **Environment:** Google Colab
*   **Scalability:** The solution uses RDDs (Resilient Distributed Datasets) and persistence strategies (`MEMORY_AND_DISK`) to ensure the algorithms scale horizontally to the full dataset, despite hardware limitations.

---

## Repository Structure
*   `AmazonMarketBasket.ipynb`: The complete executable Jupyter Notebook containing Data Loading, Preprocessing, Task A (SON), and Task B (Multistage).
*   `AMD_MarketBasketAnalysis.pdf`: The official project report detailing the methodology and experimental results.

