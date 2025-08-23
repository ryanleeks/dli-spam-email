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
