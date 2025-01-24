# Epileptic Seizure Classification from EEG Signals and 2D Images

This project utilizes advanced deep learning techniques to classify different types of epileptic seizures from EEG signals and their corresponding 2D image transformations. By employing a hybrid model of Convolutional Neural Networks (CNN) and Long Short-Term Memory networks (LSTM), it aims to improve the precision and accuracy of seizure classification.

## Project Overview

### Objective
To develop an automated and accurate system for classifying epileptic seizures using EEG signals and 2D images derived from these signals.

### Steps of the Project
1. **Data Collection**
   - Dataset: [Temple University Hospital (TUH) EEG Corpus v1.5.2](https://www.isip.piconepress.com/projects/tuh_eeg/html/downloads.shtml)
   - Contains EEG recordings of five distinct seizure types.
   - Sampling frequency: 250 Hz; 23 channels.

2. **Data Preprocessing**
   - Applied a Butterworth band-pass filter (0.5 Hz to 50 Hz).
   - Segmented EEG signals into 10-second intervals with 50% overlap.
   - Decomposed signals using **Hilbert Vibration Decomposition (HVD)**.

3. **Feature Extraction**
   - Converted high-energy subcomponents into 2D images using **Continuous Wavelet Transform (CWT)**.

4. **Model Design**
   - Built a hybrid deep learning model integrating **CNN** for spatial feature extraction and **LSTM** for temporal feature analysis.
   - Optimized using **t-SNE** for dimensionality reduction.

5. **Model Training & Evaluation**
   - Achieved an accuracy of **99.09%** and a weighted F1-score of **99.01%**.

6. **Performance Metrics**
   - Evaluated using accuracy, sensitivity, specificity, and ROC analysis.

### Tools and Technologies
- **Language:** Python 3.10.12
- **Libraries:** NumPy, SciPy, Matplotlib, Pandas, Pywt
- **Platform:** [Google Colaboratory](https://colab.research.google.com/)

## Resources
- **Dataset:** [TUH EEG Corpus v1.5.2](https://www.isip.piconepress.com/projects/tuh_eeg/html/downloads.shtml)
- **Documentation and Tutorials:**
  - [EEG Analysis with Python](https://mne.tools/stable/index.html)
  - [Introduction to Deep Learning](https://www.deeplearning.ai/)

## How to Use
1. Clone the repository.
2. Preprocess EEG signals as described in the report.
3. Train the model using the provided dataset and architecture.
4. Evaluate the model's performance on unseen data.
