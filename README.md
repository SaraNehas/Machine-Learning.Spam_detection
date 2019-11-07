### Machine-Learning.Spam_detection
# Spam detection using Scickit learn - Text Mining.

The aim of this project is to:
1. Test different algorithms and vectorizers to see the impact they have on the AUC score. 
2. Test the impact of vectorizing before or after splitting the data into a train set and a test set. 



The results are the following: 

**1. TESTING 4 COMBINATIONS OF VECTORIZERS AND ALGORITHMS:**
   - The AUC score using *CountVectorizer *and* Multinomial Naive Bayes* is **0.97**.
   
   - The AUC score using *TfidfVectorizer *and* Multinomial Naive Bayes* is **0.94**.
   
   - The AUC score using *TfidfVectorizer* and *SVM* and *adding ONE feature* is **0.96**.
   
   - The AUC score using *TfidfVectorizer* and *Logistic Regression* and *adding TWO feature* is **0.97**.

This first test shows that, in this analysis, the TfidfVectorizer is less robust than the CountVectorizer. Howerver, with som data engineering the model can give best performance results. 


**2. TESTING THE EFFECT OF VECTORIZING BEFORE AND AFTER SPLITTING DATA:**

   - Vectorizing BEFORE splitting--

      - The AUC score using CountVectorizer *before* slitting Data **0.98**.

      - The 10 words with Smallest features coefficients are: ['. ', '..', '? ', ' i', ' y', ' go', ':)', 'he', ' h', ' m'].

      - The 10 words with Largest features coefficients are: ['digit_count', 'xt', 'ww', 'ne', 'mob', 'ia', 'co', 'ar', ' x', ' ch'].

   - Vectorizing AFTER splitting--

      - The AUC score using CountVectorizer *after* slitting Data **0.98**.

      - The 10 words with Smallest features coefficients are: ['. ', '..', '? ', ' i', ' y', ' go', ':)', ' h', 'he', 'go'].

      - The 10 words with Largest features coefficients are: ['digit_count', 'xt', 'ww', 'ne', 'mob', 'ia', 'co', 'ar', ' x', ' ch'].

In this second test, the AUC scores are the same (or at least very similar). The difference is in the features that have the smallest coefficients. They are not the same on the 2 models. However the difference is so small it doesn't effect the performance of both models. 
