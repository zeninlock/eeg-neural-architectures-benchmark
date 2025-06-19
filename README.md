# EEG Neural Architectures Benchmark

This repository benchmarks deep learning models—CNN, LSTM, GRU, and hybrid architectures—for EEG-based alcoholism detection. It includes all code, trained model files, and instructions for reproducible experiments.

---

## Project Overview

- **Goal:** Compare CNN, LSTM, GRU, and hybrid models for classifying EEG signals.
- **Features:**  
  - Modular Jupyter notebooks for augmentation, training, and evaluation  
  - Advanced data augmentation (MixUp, amplitude scaling, time shifting, etc.)  
  - Pretrained model checkpoints for quick evaluation  
  - All data hosted externally for easy access
  
---

## Setup Instructions:

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/eeg-neural-architectures-benchmark.git
cd eeg-neural-architectures-benchmark
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the EEG Dataset

- [Download the dataset from Google Drive]((https://drive.google.com/drive/folders/1t3zfVfJgmhYGSzF2VmPXZhvK8HnKMaMx?usp=drive_link))

  
---

## 🔧 Running the Notebooks

**Augmentation & Preprocessing:**
- `cnn,hybrid_augmentations.ipynb`  
  Data augmentation for CNN and hybrid models
- `lstm,gru_augmentation.ipynb`  
  Data augmentation for LSTM and GRU models

**Model Training & Evaluation:**
- `pure_cnn_final.ipynb`  
  Train and evaluate the pure CNN model
- `pure_bilstm_final.ipynb`  
  Train and evaluate the BiLSTM model
- `pure_gru_final.ipynb`  
  Train and evaluate the GRU model
- `hybrid_conv1d.ipynb`  
  Train and evaluate hybrid Conv1D models
- `hybrid_conv2d.ipynb`  
  Train and evaluate hybrid Conv2D models

**Model Files:**
- `final_pure_cnn.keras`
- `final_pure_lstm.keras`
- `final_pure_gru.keras`
- `final_hybrid_conv1d.keras`
- `final_hybrid_conv2d.keras`

> **Note:** eeg_data_cleaned.npy and y.npy are raw, cleaned data files. For easeir usage the augmented and mixed dataset is also made available with proper naming.

---

## 📁 File Structure

```
.
├── cnn,hybrid_augmentations.ipynb
├── lstm,gru_augmentation.ipynb
├── pure_cnn_final.ipynb
├── pure_bilstm_final.ipynb
├── pure_gru_final.ipynb
├── hybrid_conv1d.ipynb
├── hybrid_conv2d.ipynb
├── final_pure_cnn.keras
├── final_pure_lstm.keras
├── final_pure_gru.keras
├── final_hybrid_conv1d.keras
├── final_hybrid_conv2d.keras
├── data/                # Place downloaded EEG data here
└── README.md
```

---

## 📋 Notes

- **Dataset:** UCI EEG Alcoholism Dataset (linked above)
- **Classes:** Alcoholic vs Control
- **Augmentations:** MixUp, amplitude scaling, time warping, frequency shifts, etc.
- **Best Model:** Conv2D-BiLSTM achieved 94% accuracy and AUC 0.98
- **Trained models:** Provided as `.keras` files for direct loading and evaluation
---

## 🙏 Acknowledgments

- UCI EEG Alcoholism Dataset
