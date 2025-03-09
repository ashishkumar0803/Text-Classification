# Multi-Label Text Classification for Emotion Analysis

**Task Description**

Given a target text snippet, predict the perceived emotion(s) of the speaker. Specifically, classify whether each of the following emotions apply: joy, sadness, fear, anger, surprise, or disgust. Each text snippet should be labeled as:

  - Joy (1) or no joy (0)
  - Sadness (1) or no sadness (0)
  - Anger (1) or no anger (0)
  - Surprise (1) or no surprise (0)
  - Disgust (1) or no disgust (0)

Further details on the task (Track-A) are provided at: SemEval 2025 Task 1

The sample dataset is available at the above URL. The training dataset can be accessed here: Dataset Repository. The best-performing algorithm will be evaluated on a private test set.

**Approaches**

(1) **ML**

**Prepocessing**
  - Rule-based and Feature-based Approaches
  - Use regular expressions and n-grams (word or character level - unigrams, bigrams, trigrams, etc.) as features.

**Machine Learning Methods**
  - Implement Naïve Bayes, Logistic Regression, Random Forest, and Support Vector Machine (SVM) classifiers for emotion classification.

(2) **CNN**

**Embeddings**
  - Create a custom Word2Vec model from scratch.
  - Train it on the dataset with an embedding size of 100 dimensions.

**Modeling**
  - Feedforward Neural Networks (FFNN) or
  - Recurrent Neural Networks (RNN), and
  - Long Short-Term Memory networks (LSTM).

FFNN: Maximum size of 64 units. RNN/LSTM: Maximum size of 64 units with a sequence length of 128 tokens.

**Training Setup**
  - Use Adam, AdamW, or SGD optimizer.

(3) **Transformers**

Use randomly initialized embeddings and transformer encoder layers.

**Models**
  - Used a pre-trained model (BERT or RoBERTa), consisting of 12 layers.
 
 ## Results
 | Classifier | Precision (avg macro)  | Recall (avg macro)  | F1-score (avg macro) | Code |
| ---------- | --------- | ------ | ------- |------- |
| Naïve Bayes | 0.37 | 0.22 | 0.23 | [Google colab](https://drive.google.com/file/d/1fiHpPxrVu4JxubQaE_ZUiPnkwdAMfTdn/view?usp=sharing) |
| Logistic Regression | 0.31 | 0.20 | 0.17 | Same as above |
| SVM | 0.69 | 0.29 | 0.34 | Same as above |
| Random Forest | 0.54 | 0.33 | 0.35 | Same as above |
| FFNN | 0.38 | 0.23 | 0.29 | [Google colab](https://colab.research.google.com/drive/18nf0fF8_XRGHzlWTQy34OczSgmjYVjiE?usp=sharing) |
| LSTM | 0.36 | 0.23 | 0.27 | Same as above |
| BERT | **0.76** | 0.61 | 0.65 | [Google colab](https://colab.research.google.com/drive/1KeXbYvkHEKuRgUhF9jPkmhpqy6jJRNX-?usp=sharing) |
| Roberta | 0.75 | **0.62** | **0.66** | [Google colab](https://colab.research.google.com/drive/1H0uIgXKvgVF43U3tKU8uXrAXaLUzk77Z?usp=sharing) |

**Implementation of Viterbi Algorithm**

**Objective**

Implement the Viterbi algorithm to perform Part-of-Speech (POS) tagging using the provided corpus. The implementation should also handle noisy data by exploring multiple decoding paths and dynamically adjusting emission probabilities.

**Steps**
  - HMM Setup: Used the dataset to derive hidden states (POS tags) and observable states (words).
  - Viterbi Implementation: Implement the Viterbi algorithm to decode the most probable POS tags for each sentence.
  - Noise Handling: Implement strategies to handle noise in the test data by exploring multiple decoding paths.
  - Performance Evaluation: Compare the accuracy of the baseline Viterbi algorithm vs. the noise-handled version on the provided datasets.
## Results [Google colab](https://colab.research.google.com/drive/13c-Q-2hPTJdS-wNzuV9DTGgwuxMJ52I0?usp=sharing)
Baseline Accuracy (Test Data): 0.9021885316053307

Noise-Handled Accuracy (Noisy Data): 0.8180706687859152

