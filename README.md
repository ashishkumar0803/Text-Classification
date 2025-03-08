# Text-Classification
**Text Classification Using Regular Expressions and Machine Learning Techniques**

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
  - Feedforward Neural Networks (FFNN)
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

**Implementation of Viterbi Algorithm**

**Objective**

Implement the Viterbi algorithm to perform Part-of-Speech (POS) tagging using the provided corpus. The implementation should also handle noisy data by exploring multiple decoding paths and dynamically adjusting emission probabilities.

**Steps**
  - HMM Setup: Used the dataset to derive hidden states (POS tags) and observable states (words).
  - Viterbi Implementation: Implement the Viterbi algorithm to decode the most probable POS tags for each sentence.
  - Noise Handling: Implement strategies to handle noise in the test data by exploring multiple decoding paths.
  - Performance Evaluation: Compare the accuracy of the baseline Viterbi algorithm vs. the noise-handled version on the provided datasets.
## Results    

