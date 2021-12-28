### AI4D-iCompass-Social-Media-Sentiment-Analysis-for-Tunisian-Arabizi

[Competition website](https://zindi.africa/competitions/ai4d-icompass-social-media-sentiment-analysis-for-tunisian-arabizi/leaderboard)

- This is an NLP project about Tunisian Arabizi sentiment analysis
- The goal is to classify the sentiments into 3 categories ```positive (1), negative (-1), and neutral (0)```
- Tunisian Arabizi contains different languages: [Arabizi](https://www.igi-global.com/dictionary/sentiment-analysis-of-arabic-documents/89420), French, and English
- Established a baseline with Naive Bayes which gave a good accuracy value, mainly because the dataset was highly imbalanced
- Due to the small size of the dataset, I preferred to fine-tune a bert model: experimented with different models and found that the ```bert-base-multilingual-cased``` from the ```Hugging Face``` model Hub performed better than the others.
- Added a ```Conv1D``` layer on top of the bert model, followed by a ```GlobalAveragePooling1D```
- Used ```Adam``` optimizer with 2e-5 as a learning rate and fine-tuned the model for 4 epochs.
- Tried different strategies to improve model accuracy such as layer-wise learning rate but the performance did not improve much
- Final submission on the Leaderboard ```0.8224```
- ```notebook/train.ipynb``` contains the training notebook
