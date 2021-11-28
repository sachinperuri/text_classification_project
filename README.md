# Text classification project

Authors:

- Sachin Peruri (sachin.peruri@gmail.com)
- Keyuri Raodeo (keyuri.raodeo@gmail.com)

This repo contains the NLP based text classification project worked on by the above authors. The following Kaggle dataset has been used: https://www.kaggle.com/rmisra/news-headlines-dataset-for-sarcasm-detection

Goal of the project was to correctly classify given news headlines as either "Normal" or "Sarcastic" using various ML and DL methods.

__A summary of the findings are:__

Overall, various ML models were explored using the incredible PyCaret library, with and without using NMF to reduce the dimensionality of the dataset.

- Reducing dimensionality of the dataset using Non-negative matrix factorization or NMF seemed to decrease the precision/F1-score metrics by * *5-6 percentage points** but sped up the model fitting by a lot. 

- Thus, NMF reduction can be used where performance and time spent matters most.

- Training using the full dataset took much longer but gave the highest **F1-score of 0.78** using the fine-tuned LGBM classifier (which was found to perform the best after comparing with other ML models in the first place).

- Moving to Deep learning methods, even simple sequential neural networks seemed to match or exceed the grid-searched and fine-tuned LGBM classifier. This shows the power of adding complexity to the model.

- By using BERT, validation accuracy was recorded to be **0.93 after only 1 epoch**, which again shows the power of BERT over simple neural networks.

- We can also see the potential for overfitting by using a powerful model such as BERT, as the training accuracy seemed to reach **0.977** after just 1 epoch of fine-tuning.