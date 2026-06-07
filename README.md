🛡️ CyberShield AI — Cyberbullying Detection System
Real-time toxic comment detection using NLP and Machine Learning, built with Python.

📌 Overview
CyberShield AI is a machine learning project that automatically detects whether a comment is toxic or harmful. It analyzes text input and returns a verdict, confidence score, flagged terms, and a risk breakdown across multiple categories.

🚀 Features
- Real-time toxic comment detection
- Confidence score with visual progress bar
- Risk breakdown across 4 categories — Harassment, Hate Speech, Threats, Insults
- Flagged terms highlighting
- Session history and live analytics dashboard
- Quick example inputs for testing

🧠 How It Works
1. Raw comments are cleaned and converted to numerical vectors using **TF-IDF Vectorization**
2. Bigrams (`ngram_range=(1,2)`) allow the model to detect harmful phrases, not just individual words
3. A **Logistic Regression** classifier predicts the probability of toxicity
4. If probability exceeds 50%, the comment is flagged as toxic

🗂️ Dataset
- Source: [Kaggle](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data)
- Columns used: `comment_text`, `toxic`
- Preprocessing: removed nulls, balanced classes via `class_weight='balanced'`

🛠️ Tech Stack
- Python
- Pandas
- Scikit-learn
- Gradio
- Google Colab

⚙️ How to Run
1. Open in Google Colab
2. Upload your `dataset.csv`
3. Run Cell 1 — installs dependencies and trains the model
4. Run Cell 2 — launches the Gradio UI

📊 Model Performance
Trained on 80% of dataset, tested on 20%
Metric: Precision, Recall, F1-Score (see classification_report output)

⚠️ Limitations
- Struggles with **implicit toxicity** — passive-aggressive phrases that don't contain obvious slur words (e.g. "nobody likes you, just give up")
- Performance depends heavily on training data quality and size

🔮 Future Improvements
- Replace Logistic Regression with a transformer-based model like **BERT** for better context understanding
- Add multilingual support
- Deploy as a standalone web app

👩‍💻 Author
Made by **Esha** as part of an AI/ML course project.
