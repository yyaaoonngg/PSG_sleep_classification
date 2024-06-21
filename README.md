# 멀티모달 생체신호를 이용한 인공지능 기반 수면 단계 분류 및 이미지 생성 🛌🏻
본 프로젝트는 수면 뇌파 데이터를 포함한 다양한 생체신호 데이터를 종합적으로 분석하고, 이를 기반으로 수면 상태를 시각화한다. 이미지나 비디오를 보는 중 측정하여 label이 있는 뇌파를 기반으로 이미지를 재구성하는 연구는 많이 진행되었으나, 우리 데이터는 수면 생체 신호를 이용하여 label이 없는 상태에서 데이터 특성을 바탕으로 이미지를 생성한다. 이는 뇌졸중 환자와 같이 의사소통이 불가능한 사람들의 의사 파악 등에 활용할 수 있다는 점에서 의의가 있다.
우리 프로젝트는 먼저 EEG, EMG, EOG, ECG 신호를 CNN+LSTM 모델을 통해 수면단계를 분류하고, 각 신호에 대하여 feature extraction을 진행한다. 이후 생성형 AI 기술을 사용하여, 추출한 특성들을 바탕으로 시각화된 이미지를 산출한다.

# Data
Haaglanden Medisch Centrum sleep staging database

URL: https://physionet.org/content/hmc-sleep-staging/1.1

# Data Preprocessing
Band-Pass Filtering, Notch Filtering, Wavelet denoising, Resampling, Z-score normalization('./_Preprocessing.ipynb')

<img width="931" alt="Screenshot 2024-06-18 at 14 35 52" src="https://github.com/hoho9337/PSG_sleep_classification/assets/97961767/e96d5673-7713-49b3-b95d-cec7eebbaed0">

# Model
2 layers of 1D-CNN + LSTM ('./tensor_to_CNN_LSTM.ipynb')

Preprocessed .edf data was processed into pytorch tensors ('./edf_to_tensor.ipynb')

![model](https://github.com/hoho9337/sleep-EOG-analysis/assets/97961767/5ccb71ae-4735-4268-a8e3-ad99b4fbf1f8)


# 결과
![image](https://github.com/yyaaoonngg/PSG_sleep_classification/assets/97872145/03267157-657b-4e90-9773-d5f38d192acb) <br>
[서비스 화면]
![image](https://github.com/yyaaoonngg/PSG_sleep_classification/assets/97872145/2b2c0012-af27-451d-ad5d-17f3842dda3f) <br>
[이미지 출력 결과]
