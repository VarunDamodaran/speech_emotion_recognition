# Audio Emotion Recognition Project

This project focuses on audio emotion recognition using various datasets. The goal is to classify emotions from audio files. This README provides an overview of the code, datasets used, and key functionalities.

## Table of Contents

- [Installation](#installation)
- [Datasets](#datasets)
- [Data Preparation](#data-preparation)
- [Feature Extraction](#feature-extraction)
- [Spectrogram Visualization](#spectrogram-visualization)
- [Model Training](#model-training)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Installation

To run this project, you need to install the required libraries. Use the following commands to set up your environment:

```bash
!apt-get update
!apt-get install -y libsndfile1
pip install librosa seaborn tensorflow keras
```

## Datasets

The project uses the following datasets:

1. **RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)**: Contains 24 professional actors (12 male, 12 female) vocalizing two lexically-matched statements in a neutral North American accent.

2. **CREMA-D (Crowd-Sourced Emotional Multimodal Actors Dataset)**: Contains 7,442 original clips from 91 actors.

3. **SAVEE (Surrey Audio-Visual Expressed Emotion)**: Contains recordings from 4 male actors expressing 7 different emotions.

4. **TESS (Toronto Emotional Speech Set)**: Contains 200 target words spoken in the carrier phrase "Say the word _" by two actresses.

## Data Preparation

The data preparation involves reading the audio files from the datasets and extracting relevant information such as file paths and emotions. The code performs the following steps:

1. **Mount Google Drive**: To access the datasets stored in Google Drive.
2. **Load RAVDESS Dataset**: Extracts file paths and emotions, and stores them in a DataFrame.
3. **Load CREMA-D Dataset**: Extracts file paths and emotions, and stores them in a DataFrame.
4. **Load SAVEE Dataset**: Extracts file paths and emotions, and stores them in a DataFrame.
5. **Load TESS Dataset**: Extracts file paths and emotions, and stores them in a DataFrame.
6. **Combine All Datasets**: Combines the DataFrames from all datasets into a single DataFrame.

## Feature Extraction

Various audio features are extracted to represent the audio signals. The features include:

1. **RMS Energy**: Root Mean Square energy of the audio signal.
2. **Zero Crossing Rate (ZCR)**: The rate at which the signal changes sign.
3. **Band Energy Ratio (BER)**: The ratio of energy in different frequency bands.
4. **Spectral Centroid**: The center of mass of the spectrum.
5. **Bandwidth**: The width of the band in the spectrum.
6. **Mel-Frequency Cepstral Coefficients (MFCCs)**: A representation of the short-term power spectrum of sound.

## Spectrogram Visualization

The project includes code for visualizing the spectrograms of audio signals. This includes:

1. **Magnitude Spectrum**: The magnitude of the Fourier Transform of the signal.
2. **Spectrogram**: A visual representation of the spectrum of frequencies of the signal as it varies with time.
3. **Log-Amplitude Spectrogram**: The logarithm of the amplitude of the spectrogram.
4. **Mel Spectrogram**: A spectrogram where the frequencies are converted to the Mel scale.

## Model Training

The project utilizes various machine learning models for emotion recognition from audio signals. The models include:

1. **Convolutional Neural Networks (CNNs)**: For extracting spatial features from spectrograms.
2. **Long Short-Term Memory (LSTM)**: For capturing temporal dependencies in the audio signals.
3. **GRU (Gated Recurrent Unit)**: An alternative to LSTM for capturing temporal dependencies.

The models are built using Keras and TensorFlow.

## Results

The project evaluates the performance of the models using metrics such as confusion matrix and classification report. The results show the accuracy and other performance metrics of the emotion recognition models.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
