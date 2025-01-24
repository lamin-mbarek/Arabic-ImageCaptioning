# Arabic Image Captioning

## Project Overview
This project focuses on generating descriptive captions for images in Arabic using deep learning techniques. The implementation leverages advanced Natural Language Processing (NLP) and Computer Vision (CV) methods to achieve accurate and meaningful captions for a diverse set of images.

## Features
- **Arabic Text Processing**: Handles the complexities of Arabic script, including diacritics, right-to-left text direction, and ligatures.
- **Efficient Feature Extraction**: Utilizes EfficientNetB0 for extracting image features.
- **Caption Generation**: Employs an LSTM-based sequence model for generating captions.
- **Evaluation Metrics**: BLEU scores (BLEU-1 to BLEU-4) to evaluate the quality of generated captions.

## Dataset
- **Dataset Used**: Flickr8k dataset.
- **Modifications**: The dataset was cleaned and augmented with captions in Arabic.

## Project Workflow

### 1. Data Preprocessing
- Cleaned the Arabic captions by removing diacritics, punctuations, and stop words.
- Converted numerical data into Arabic words.
- Reshaped and normalized Arabic text to align with machine learning models.

### 2. Feature Extraction
- Used **EfficientNetB0**, pre-trained on ImageNet, to extract features from images.
- Features were stored in a serialized format for efficient training.

### 3. Model Architecture
- **Visual Feature Extractor**:
  - Dense and Dropout layers to process the features extracted from images.
- **Textual Model**:
  - Embedding and LSTM layers for processing Arabic captions.
- **Decoder**: Combines visual and textual representations to predict the next word in the caption sequence.

### 4. Training
- Model trained for 15 epochs using a generator that prepares sequences and image features on the fly.
- Optimized using categorical cross-entropy loss and Adam optimizer.

### 5. Evaluation
- Evaluated the model using BLEU scores to assess the fluency and relevance of generated captions.

## Example Outputs
#### Generated Caption
![Image](https://github.com/user-attachments/assets/b8e73bb2-02d7-4d1e-88f1-215e6f8facb9)


