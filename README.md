## Image Captioning

### Objective: Design a CNN-LSTM system for image captioning, comparing baseline and modified baseline models.

### Dataset: Utilized the Flickr8K dataset with 8,000 images, each accompanied by five captions.

### Data Preprocessing:

Cleaned captions by lowercasing and removing special tokens.
Selected words occurring at least 10 times for robustness.
Added 'startseq' and 'endseq' tokens to define caption boundaries.
Data Preparation:

Encoded words into fixed-sized vectors using wordToIndex and indexToWord dictionaries.
Used data generators for efficient processing of large datasets.
Embeddings:

### Vision Embedding: Averaged image feature vector from InceptionV3 for baseline and ViT for modified baseline.
### Word Embedding: Utilized pre-trained GLoVe word embeddings.

### Model Architecture:

CNN-LSTM model with InceptionV3 for baseline and ViT for modified baseline.
LSTM for sequential data processing.
Used Categorical Cross Entropy loss and Adam optimizer.

### Training:

### Baseline: Trained for 20 epochs with batch size 3.
### Modified Baseline: Trained for 12 epochs with batch size 4.

### Evaluation:

### Metrics: BLEU and METEOR scores on Flickr8K test data.
#### Comparison: Baseline vs. Modified Baseline.

### Results:

BLEU Scores: Baseline - 0.5505, Modified Baseline - 0.5603.
METEOR Scores: Baseline - 0.3156, Modified Baseline - 0.2017.
Observations:

Modified baseline showed improved BLEU scores, attributed to richer image representations.
Baseline had better METEOR scores, possibly due to higher-dimensional image embeddings.
Visual inspection revealed biases in predicted words, indicating potential model limitations.
Conclusion: The modified baseline exhibits enhanced performance in certain aspects, emphasizing the importance of image representations in image captioning.
