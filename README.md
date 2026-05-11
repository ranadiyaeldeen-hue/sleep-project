# Deep Learning-Based Sleep Stage Classification Using EOG-R

Automatic sleep stage classification project using a single-channel EOG-R signal.


## Project Description
The goal of this project is to classify sleep stages automatically using deep learning techniques while reducing the complexity of traditional multi-channel sleep analysis systems.

A hybrid CNN-BiLSTM model was developed to learn:
- Spatial features from EOG signals
- Temporal relationships between sleep stages

The project includes:
- Signal preprocessing
- Data preparation
- Model training
- Performance evaluation
- Visualization of results

## Dataset
Dataset:
- MESA Sleep Study (NSRR)

Signal Used:
- EOG-R Channel

Sleep Stages:
- Wake
- Stage 1
- Stage 2
- Stage 3
- REM

Signal Information:
- Sampling Frequency: 256 Hz
- Epoch Length: 30 seconds
- Samples per Epoch: 7680

## Preprocessing Steps
- Bandpass filtering (0.3–35 Hz)
- Z-score normalization
- Epoch segmentation
- XML annotation parsing

## Model Architecture
Implemented Model:
- CNN-BiLSTM

Main Components:
- Conv1D layers
- Batch Normalization
- MaxPooling
- Bidirectional LSTM
- Dropout
- Dense layers
- Softmax classifier

## Training Configuration
- Optimizer: Adam
- Learning Rate: 0.001
- Batch Size: 64
- Epochs: 30
- Loss Function: Categorical Cross-Entropy

Techniques Used:
- Early Stopping
- ReduceLROnPlateau
- Class weighting

 ## Results

Training Performance:
- Final Training Accuracy: 86.54%
- Final Validation Accuracy: 69.38%
- Best Validation Accuracy: 80.83% (Epoch 11)

Test Performance:
- Test Accuracy: 80.41%

Observations:
- Strong performance in Wake and REM classification
- Lower accuracy in Stage 1 detection
- EOG-R outperformed EOG-L
