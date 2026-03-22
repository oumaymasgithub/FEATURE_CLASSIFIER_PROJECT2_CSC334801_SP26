# FEATURE_CLASSIFIER_PROJECT2_CSC334801_SP26
# Model Comparison

This repository contains the implementation and evaluation of multiple models for text classification. The models included are CNN, LSTM, GRU, and MLP. Each model has its architecture, techniques, and results summarized below.


## 1. CNN

### Model Architecture
- Input layer: sequences of tokenized text
- Convolutional layers with ReLU activation
- MaxPooling layers for downsampling
- Fully connected (dense) layer
- Output layer: softmax activation for binary classification

### Techniques Applied
- Tokenization and padding of input sequences
- Dropout regularization
- Early stopping
- Adam optimizer with categorical crossentropy loss
- Optional: pretrained Word2Vec embeddings

### Results
- Accuracy: 0.8902
- Class 0: Precision 0.91, Recall 0.87, F1-score 0.89
- Class 1: Precision 0.87, Recall 0.91, F1-score 0.89

### Observations
- Strong balance between classes
- Efficient for feature extraction in text sequences
- Faster training compared to RNN-based models

## 2. LSTM

### Model Architecture
- Input layer: sequences of tokenized text
- Embedding layer (optional pretrained embeddings)
- LSTM layer(s) for sequential processing
- Fully connected (dense) layer
- Output layer: softmax activation for binary classification

### Techniques Applied
- Tokenization and padding
- Dropout regularization
- Early stopping
- Adam optimizer
- Captures sequential dependencies

### Results
- Accuracy: 0.8708
- Class 0: Precision 0.84, Recall 0.92, F1-score 0.88
- Class 1: Precision 0.91, Recall 0.83, F1-score 0.87

### Observations
- Good recall for class 0
- Slightly slower training than CNN
- Effective at capturing sequential patterns



## 3. GRU

### Model Architecture
- Input layer: sequences of tokenized text
- Embedding layer (optional pretrained embeddings)
- GRU layer(s) for sequential processing
- Fully connected (dense) layer
- Output layer: softmax activation for binary classification

### Techniques Applied
- Tokenization and padding
- Dropout regularization
- Early stopping
- Adam optimizer
- Efficient sequential modeling with GRU units

### Results
- Accuracy: 0.8826
- Class 0: Precision 0.90, Recall 0.86, F1-score 0.88
- Class 1: Precision 0.87, Recall 0.91, F1-score 0.89

### Observations
- Balanced performance across classes
- Slightly better recall for class 1 than CNN
- Captures sequential dependencies efficiently



## 4. MLP

### Model Architecture
- Input layer: flattened feature vector
- Dense layers with ReLU activation
- Dropout for regularization
- Output layer: softmax activation for binary classification

### Techniques Applied
- Standard scaling/normalization of features
- Dropout regularization
- Adam optimizer with categorical crossentropy loss
- Simple fully connected network for baseline performance

### Results
- Accuracy: 0.7776
- Class 0: Precision 0.77, Recall 0.79, F1-score 0.78
- Class 1: Precision 0.79, Recall 0.77, F1-score 0.78

### Observations
- Simpler architecture; lower performance than CNN or RNN models
- Balanced performance across classes
- Useful as a baseline for comparison
