# Fake-news-Icon-
Fake News &amp; Hate Speech Detection in Hinglish (Hindi-English Code-Mixed Text)

 Decoding Fake Narratives in Spreading Hateful Stories (Faux-Hate)

 
 The project performs **multi-label classification** on Hinglish text:

- **Fake:** Is the content fake? (`1 = Fake`, `0 = Not Fake`)
- **Hate:** Does it contain hate speech? (`1 = Hate Speech`, `0 = Neutral`)
- **Target:** How targeted is the content? (`0 to 3`, higher = more specific targeting)
- **Severity:** How harmful is the content? (`0 to 3`, higher = more severe)

In real-world datasets, the number of non-hate or real news examples is usually much higher than fake or hateful content. This **class imbalance** can make the model biased toward majority classes.

Solution: Oversampling

We use techniques like **SMOTE** and **RandomOverSampling** to balance the dataset:

- Before and after **visualizations** of class distribution help us:
  - Understand the imbalance.
  - Confirm that oversampling methods are working.
  - Ensure the model learns from **minority classes** effectively. 

## 📈 Model Performance

| **Label**     | **Accuracy** | **Precision** | **Recall** | **F1-Score** |
|---------------|--------------|---------------|------------|--------------|
| Fake News     | 0.7794       | 0.78          | 0.78       | 0.78         |
| Hate Speech   | 0.7825       | 0.78          | 0.78       | 0.78         |
| Target        | 0.7412       | 0.74          | 0.74       | 0.74         |
| Severity      | 0.7418       | 0.74          | 0.74       | 0.74         |


## Models Used

-  **Multilingual BERT** (`bert-base-multilingual-cased`)
  - Fine-tuned on Hinglish text.
- **Multinomial Naive Bayes**
  - Used with TF-IDF features.
  - Lightweight baseline model.
