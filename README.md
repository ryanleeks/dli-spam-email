# Deep Learning for Intrusion Detection <br>
This is a repository for **Fake Job Detection Model** (DLI Assignment) <br>
The model is trained, tested, and evaluated in Google Colab and meets the assignment requirements including metrics, visualizations, and proper documentation.
_______

# Group W Members
| Name                | Student ID | Role                |
| ------------------- | ---------- | ------------------- |
| Dang Ming Yao       | TP064621   | Data Lead, GUI Lead |
| Lee Mun Hin Ian     | TP062026   | Documentation Lead  |
| Ryan Lee Khang Sern | TP062364   | Evaluation Lead     |
| Tan Chang Yau       | TP073578   | Model Lead          |
_______

# Project Objective <br>
To protect job seekers from scams by applying deep learning techniques to analyze job descriptions and flag suspicious listings.
_______

# Training Setup <br>
Training Optimization: Used mixed-precision training with autocast for faster computation and reduced memory usage.

Stability: Applied gradient scaling during forward and backward passes to maintain numerical stability.

Validation: Conducted after each epoch with dynamic threshold tuning to maximize F1-score for the minority (fraudulent) class.

Overfitting Control: Implemented early stopping (patience = 2 epochs).

Model Selection: Saved the best model based on improvements in fraudulent class F1-score.
_______

# Models
Model Used: DistilBERT – a lightweight transformer that keeps most of BERT’s accuracy but reduces parameters and training time.

Suitability: Well-suited for text classification tasks due to strong contextual understanding.

Input Data: Preprocessed job ads, with text fields (title, company profile, description) concatenated and cleaned of noise.

Tokenization: Used DistilBERT’s built-in tokenizer to convert text into subword tokens for model processing.
_______

# Dataset Information
- Name : [Real / Fake Job Posting Prediction (Kaggle)](https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction/data)
- Source : Employment Scam Aegean Dataset (EMSCAD)
- Size :  17,880 rows - Legit(17,014)/Fake(886)
- License : [CC0: Public Domain](https://creativecommons.org/publicdomain/zero/1.0)
_______

# Evaluation
- Confusion Matrix
<img width="722" height="583" alt="image" src="https://github.com/user-attachments/assets/180b84ff-adf3-4c31-9a8f-d2f69b65129c" />

- Roc Curve
<img width="611" height="609" alt="image" src="https://github.com/user-attachments/assets/7db51d7f-b5d1-446a-826a-0dab60c39298" />

_______

# GUI Output
- Legit
<img width="944" height="535" alt="image" src="https://github.com/user-attachments/assets/04aa2ca7-079f-4e4b-aa4a-1e54e40a2619" />

- Fraud
  <img width="940" height="543" alt="image" src="https://github.com/user-attachments/assets/c41764a1-3761-4f35-9b1d-cbdc5ae049b4" />

