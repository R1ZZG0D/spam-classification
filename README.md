# 📩 SMS Spam Classifier

This project is a **machine learning pipeline** that detects **spam SMS messages** using natural language processing (NLP) techniques and a Naive Bayes classifier. The model is trained on the [UCI SMS Spam Collection Dataset](https://archive.ics.uci.edu/dataset/228/sms+spam+collection).

---

## 🔍 Project Highlights

- **Text Preprocessing** with NLTK: tokenization, stopword removal, stemming
- **Feature Extraction** using CountVectorizer with unigrams and bigrams
- **Classification Model**: Multinomial Naive Bayes
- **Hyperparameter Tuning** with GridSearchCV
- **Spam Prediction** with probability scores
- **Model Persistence** using `joblib`

---

## 🗃️ Dataset

The dataset contains **5,574 labeled SMS messages**, split into `spam` and `ham` (not spam). It is publicly available from the UCI Machine Learning Repository.

- Downloaded and extracted using `requests` and `zipfile`
- Stored in: `sms_spam_collection/SMSSpamCollection`

---

## 🛠️ How to Run

### 1. Clone this repository
```bash
git clone https://github.com/YOUR_USERNAME/spam-classification.git
cd spam-classification

### 2. Create and activate a virtual environment
python -m venv myenv
# Windows
myenv\Scripts\activate
# macOS/Linux
source myenv/bin/activate

### 3. Install dependencies
pip install -r requirements.txt

### 4. Run the scripts

📥 Download & extract the dataset
python dataset.py

🤖 Train and evaluate the model
python main.py

---

## 📊 Example Predictions

The trained model evaluates custom SMS messages and returns:

Spam/Not-Spam label

Probability scores for each class

Example:

Message: Congratulations! You've won a $1000 Walmart gift card.
Prediction: Spam
Spam Probability: 0.98
Not-Spam Probability: 0.02

