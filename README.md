# Sleep-PSG-analysis
Preprocessing and analyzing PSG signals(EEG(4), EOG(2), EMG(1), ECG(1)) for multi-modal AI and automated sleep staging

# Data
Haaglanden Medisch Centrum sleep staging database
URL: https://physionet.org/content/hmc-sleep-staging/1.1

# Preprocessing
Band-Pass Filtering, Notch Filtering, Wavelet denoising, Resampling, Z-score normalization
<img width="931" alt="Screenshot 2024-06-18 at 14 35 52" src="https://github.com/hoho9337/PSG_sleep_classification/assets/97961767/e96d5673-7713-49b3-b95d-cec7eebbaed0">


# Model
2 layers of 1D-CNN + LSTM
![model](https://github.com/hoho9337/sleep-EOG-analysis/assets/97961767/5ccb71ae-4735-4268-a8e3-ad99b4fbf1f8)
