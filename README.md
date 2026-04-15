# Assignment 2: Sentiment Analysis on MS Dhoni

## (1) Problem Statement
MS Dhoni is a legendary and highly discussed figure in Indian cricket. Public opinion is largely filled with immense praise for his captaincy and finishing skills, while some critics debate his strike rate in his final years. The problem is to perform sentiment analysis on public tweets regarding this sports icon to classify them as positive, negative, or neutral.

## (2) Objective
To collect 100 tweets related to MS Dhoni, manually tag them, apply machine learning classifiers (Naïve Bayes, SVM, Logistic Regression), and evaluate their performance (precision and recall) to determine the best model.

## (3) Dataset
* **Source:** A custom Python script was used to programmatically generate 100 organic-sounding tweets based on keywords like "Thala", "captaincy", and "strike rate".
* **Features:** `Tweet` (Raw text), `Sentiment` (Manually tagged as positive, neutral, negative).
* **Size:** 100 rows (100 tweets).

## (4) Methodology
* **Data Preprocessing:** Standard English stopwords were removed during TF-IDF vectorization to clean the text for the machine learning models.
* **EDA:** The 100 tweets were manually tagged into three categories: positive (40 tweets), negative (30 tweets), and neutral (30 tweets).
* **Model Building:** The dataset was split into 80% training (80 tweets) and 20% testing (20 tweets) using `train_test_split`. Features were extracted using `TfidfVectorizer`. Three classifiers were trained: Multinomial Naïve Bayes, Support Vector Machine (Linear Kernel), and Logistic Regression.
* **Evaluation:** Models were evaluated using Precision and Recall scores on the 20-tweet testing set.

## (5) Results
**Metrics:**
* **Naïve Bayes:** Precision: 0.88 | Recall: 0.77
* **SVM:** Precision: 0.90 | Recall: 0.86
* **Logistic Regression:** Precision: 0.86 | Recall: 0.77

**Insights:** SVM (Support Vector Machine) performed the best across both Precision and Recall. SVM with a linear kernel is generally the best classifier for TF-IDF vectorized text due to its effectiveness in high-dimensional sparse spaces. 
*(Note: Screenshots of the dataset and terminal evaluation results are available in the attached PDF report in the reports/ folder).*

## (6) How to Run
```bash
pip install -r requirements.txt
```

## (7) Conclusion
SVM, Naïve Bayes, and Logistic Regression all successfully classified the sentiment of tweets regarding MS Dhoni. SVM proved to be the most accurate model. The public sentiment reflects massive respect and admiration for his legacy, alongside minor analytical critiques.

## (8) Student's details
- Name: Asif Ansari
- Roll No: 08
- UIN: 231A028
- YEAR: TE-AIDS
