# IT9002 - Natural Language Processing Project
![Alt text for accessibility](https://github.com/israa-tageldin/NLP-Project/blob/main/banner.png?raw=true)

---

## Project Overview
This project investigates the relationship between customer **star ratings** and the **sentiment expressed in review text** using the Amazon *Health & Personal Care* dataset (2023).

By comparing an independent **BERT-based sentiment model** with **rating-derived machine learning classifiers**, the study evaluates agreement, disagreement, and proposes a **combined reliability indicator** for improved customer insight.

---

## Dataset
- Source: Amazon Reviews – *Health & Personal Care* (2023) https://amazon-reviews-2023.github.io/
- Records: 11,477 reviews  
- Key fields:
  - `reviews` – cleaned combined title and text  
  - `star_rating`  
  - Derived label: `rating_polarity_3`

---

## Models Used

### Text-Based Sentiment
- **BERT / RoBERTa Transformer**  
  - Model: `cardiffnlp/twitter-roberta-base-sentiment-latest`  
  - Output classes: `negative`, `neutral`, `positive`

### Rating-Based Sentiment (TF-IDF + ML)
| Model | Description |
|------|-------------|
| Logistic Regression | Linear baseline classifier |
| Support Vector Machine (SVM) | Robust classifier for sparse text |
| Multinomial Naïve Bayes (MNB) | Probabilistic NLP benchmark |

---

## How to Run

Open the Colab notebook.
Run all cells sequentially from Task 1 to Task 6.
Final predictions will be stored in the dataframe for analysis.

---

## Requirements

```bash
pip install pandas numpy scikit-learn transformers torch tqdm matplotlib seaborn nltk



