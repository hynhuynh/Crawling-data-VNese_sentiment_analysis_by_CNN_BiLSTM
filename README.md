# Crawling data and Vietnamese sentiment analysis by CNN and LSTM
## 1. Goal:
Developing an effective model for classifying the sentiment of Vietnamese text, specifically focusing on Vietnamese customer reviews related to lipstick products. The primary objective is to accurately determine whether a given review expresses positive or negative sentiment.
## 2. Method:
- For Web Scraping, this project initially collected a dataset of customer reviews by utilizing Selenium, a web automation tool, to scrape data from Tiki and JSON request to obtain data from Shopee.
- Adopt deep learning techniques and TensorFlow Keras for data preprocessing and model development.
- Model architecture: combined Convolutional Neural Networks (CNN) and Bidirectional Long Short-Term Memory networks (Bi-LSTM) to effectively classify the sentiment in customer reviews. This leverages the strengths of both CNNs and LSTMs to improve the model's ability
to learn and extract features from text. CNN is good at capturing local patterns/features while Bi-LSTM can capture information from both past and future contexts.
## 3. Main Steps:
- Data Collection: Crawled customer reviews from Shopee using JSON requests to obtain a diverse dataset for training, testing, and validation.
- Data Preprocessing: Apply TensorFlow and Keras for data preprocessing, including text tokenization, remove accent and padding sequences,...
- Model Building: Create a sentiment analysis model using a combination of CNN and Bi-LSTM layers to capture complex patterns and dependencies in the text data.
- Model Training: Train the deep learning model on the preprocessed dataset with EarlyStopping and ReduceLROnPlateau to prevent overfitting.
- Model Evaluation: Evaluate the accuracy and performance of sentiment analysis approaches by precision, recall and f1-score.
- Utilize Model: Apply for new dataset to predict sentiments for customer reviews from Tiki.
## 4. Result:
### 4.1. Model Evaluation:
**Confusion matrix and classification report:**

![image](https://github.com/hynhuynh/Crawling-data-and-Vietnamese_sentiment_analysis_by_CNN_and_Bi_LSTM/assets/74954965/f12eb096-9b79-4a58-9e93-3e60a74403e5)

Class 0 (Positive Class):
- Precision: 0.89 - The model has a high precision for predicting positive instances, indicating that when it predicts positive sentiment, it is often correct (89% precision).
- Recall: 0.90 - The recall for positive sentiment is high, showing that the model captures a significant portion of the actual positive instances (90% recall).
- F1-Score: 0.90 - The F1-score for positive sentiment is well-balanced, reflecting a good trade-off between precision and recall (90%).

Class 1 (Negative Class):
- Precision: 0.84 - The precision for predicting negative sentiment is still good, indicating that when the model predicts negative sentiment, it is often correct (84% precision).
- Recall: 0.83 - The recall for negative sentiment is relatively lower, suggesting that the model misses some of the actual negative instances (83% recall).
- F1-Score: 0.84 - The F1-score for negative sentiment is reasonable, but there is room for improvement in capturing more actual negative instances (84%).
Accuracy: Overall accuracy of the model: 0.87 (87% of instances are correctly classified).

**==> The model performs well in distinguishing both positive and negative comments. The high precision and recall values indicate a good balance between identifying positive and negative instances.**
### 4.2. Utilize Model:

![image](https://github.com/hynhuynh/Crawling-data-and-Vietnamese_sentiment_analysis_by_CNN_and_Bi_LSTM/assets/74954965/36dcd465-15dc-4481-9300-fb846650e34f)
