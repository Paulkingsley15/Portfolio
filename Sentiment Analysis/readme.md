# Amazon Reviews Sentiment Analysis

## Project Overview

This project focuses on performing sentiment analysis on a dataset of Amazon reviews. By leveraging Natural Language Processing (NLP) techniques and machine learning models, we aim to classify the reviews as either positive or negative, providing insights into customer satisfaction.

### Files Included:
- **NLP.ipynb**:
  This is the main Jupyter notebook that contains the following:
  - Data loading and preprocessing.
  - Exploratory data analysis (EDA) on Amazon reviews.
  - Building and evaluating sentiment analysis models using transformers from Hugging Face, specifically using RoBERTa-based models.

- **Amazon Reviews Dataset**:
  This dataset includes a collection of reviews from Amazon users, with sentiment labels assigned to each review (positive or negative).
- The data set it too large to add to Github
    
### Key Features:
1. **Text Preprocessing**:
   - Tokenization of reviews using transformers.
   - Removing unwanted characters and stopwords.
   - Normalization of text data for analysis.

2. **Exploratory Data Analysis (EDA)**:
   - Word frequency analysis.
   - Sentiment distribution (positive vs negative).
   - Common n-grams and word clouds for positive and negative reviews.

3. **Modeling**:
   - Fine-tuning a pre-trained RoBERTa model for sentiment classification.
   - Evaluation of model performance using metrics such as accuracy, precision, recall, and F1-score.

4. **Sentiment Prediction**:
   - Use of the fine-tuned model to predict the sentiment of new, unseen reviews.

### Dependencies:
- **Python 3.x**
- **Jupyter Notebook**
- **Transformers (Hugging Face)**: `pip install transformers`
- **Torch (PyTorch)**: `pip install torch`
- **Pandas**: `pip install pandas`
- **NLTK**: `pip install nltk`
- **Matplotlib/Seaborn**: For visualization of data.

### How to Run:
1. **Install dependencies** (if not already installed):
   ```bash
   pip install transformers torch pandas nltk matplotlib seaborn
Open the Jupyter Notebook:

bash
Copy code
jupyter notebook NLP.ipynb
Run the notebook: Follow the instructions in the notebook to run each cell. The notebook will guide you through the data preprocessing, model training, and evaluation steps.

Results:
The model achieves an accuracy of around [accuracy percentage]% on the test data.
Commonly occurring positive and negative words were visualized using word clouds.
The fine-tuned RoBERTa model effectively classifies Amazon reviews as positive or negative based on the text content.
Future Improvements:
Experimenting with other transformer models like BERT or GPT.
Further hyperparameter tuning to improve model performance.
Expanding the dataset to include more reviews and categories.