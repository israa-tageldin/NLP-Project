# IT9002 - Natural Language Processing Project
![Alt text for accessibility](https://github.com/israa-tageldin/NLP-Project/blob/main/banner.png?raw=true)

---

## Project Overview
This project investigates the relationship between customer **star ratings** and the **sentiment expressed in review text** using the Amazon *Health & Personal Care* dataset (2023).

By comparing an independent **BERT-based sentiment model** with **rating-derived machine learning classifiers**, the study evaluates agreement, disagreement, and proposes a **combined reliability indicator** for improved customer insight.

---

## Objectives
- Compare text-based sentiment and rating-based sentiment predictions.
- Analyse linguistic patterns behind agreement and disagreement.
- Propose a hybrid **sentiment reliability signal** for more trustworthy customer insight.

---

## Dataset
- Source: Amazon Reviews – *Health & Personal Care* (2023)
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

## 📊 Outputs

| Column | Description |
|--------|-------------|
| `bert_sentiment_3` | Text-based sentiment |
| `rating_polarity_3` | Rating-derived polarity |
| `pred_lr` | Logistic Regression prediction |
| `pred_svm` | SVM prediction |
| `pred_mnb` | Naïve Bayes prediction |
| `bert_score` | BERT confidence score |

---

## Reliability Indicator

| Pattern | Reliability |
|--------|-------------|
| All models agree | Very High |
| Rating models agree, BERT differs | High |
| Partial rating disagreement | Medium |
| Rating models disagree | Low |
| All disagree | Very Low |

---

## Requirements

```bash
pip install pandas numpy scikit-learn transformers torch tqdm matplotlib seaborn
