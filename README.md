# cloud-sentiment-analysis-sagemaker

# Project Overview
This project applies an end-to-end sentiment analysis pipeline to the Amazon Fine Food Reviews dataset, combining NLP preprocessing, user anonymization, sentiment classification with Amazon Comprehend and machine learning models, data visualizations, and deployment through AWS SageMaker.

# Architecture
The workflow leverages AWS cloud services for scalable sentiment analysis:

	1.	Reviews are uploaded to a customer review bucket.
	2.	A Lambda function triggers the Amazon Comprehend API for sentiment analysis.
	3.	Results are stored in a sentiment folder in S3.
	4.	Amazon Athena is used to query and analyze sentiment results interactively.

⸻

# Features	
    • Text Preprocessing: cleaning, stopword removal, tokenization, lemmatization.
	•	User Anonymization: SHA-256 hashing for privacy.
	•	Sentiment Analysis:
	•	Amazon Comprehend (cloud NLP API).
	•	Machine Learning models (Naive Bayes, SVM).
	•	Feature Engineering: TF-IDF vectorization.
	•	Data Visualization: Sentiment distribution, word clouds, review length analysis.
	•	Cloud Deployment: Deployment workflow on AWS SageMaker.

⸻

# Dataset
The project uses the Amazon Fine Food Reviews dataset (Kaggle).

	•	Approximately 568,000 reviews.
	•	Features: review text, score, helpfulness, product information.

⸻

# Results
	•	Naive Bayes Accuracy: ~85%
	•	SVM Accuracy: ~89.4%
	•	Amazon Comprehend: Strong performance but with slight bias toward positive sentiment.

⸻

# Tech Stack
	•	Python: pandas, scikit-learn, NLTK, spaCy, matplotlib, seaborn
	•	Cloud: AWS SageMaker, Amazon Comprehend, boto3
	•	Visualization: WordCloud, matplotlib

⸻

# Ethical Considerations
	•	User privacy was protected through SHA-256 hashing.
	•	Bias in cloud NLP models was evaluated and documented.
