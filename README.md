# Speech Emotion Recognition (SER) with RAVDESS Dataset

A comparative study of SVM and CNN models for emotion recognition from speech using **Mel-Frequency Cepstral Coefficients (MFCCs)**.

## 📁 Dataset
**Source:** [RAVDESS Dataset](https://doi.org/10.1371/journal.pone.0196391)  
**Context:** 24 professional actors (12M/12F) performing 8 emotions  
**Emotions:** Neutral, Calm, Happy, Sad, Angry, Fearful, Surprise, Disgust  
**Ethics:** IRB-approved recordings with informed consent

## 🛠️ Methodology
### 1. Feature Extraction
- **MFCCs (Mel-Frequency Cepstral Coefficients)**
  - 2D time-frequency representations
  - Mimics human auditory perception
  - Example MFCC visualization included in the notebook

### 2. Model Architecture
| Model | Type | Key Characteristics |
|-------|------|---------------------|
| SVM | Traditional | Linear kernel, L2 regularization |
| **CNN** | Deep Learning | 4 Conv layers, MaxPooling, Dropout |

### 3. Training Details
- 288 audio samples (speech only)
- 80-20 train-test split
- Adam optimizer (CNN)
- 50 epochs

## 📊 Key Results
### Model Comparison
| Metric | SVM | CNN |
|--------|-----|-----|
| Accuracy | 56% | **60%** |
| Weighted F1 | 0.53 | **0.60** |
| Best Class | Female Surprise (F1=0.86) | Female Surprise (F1=0.84) |

### Specialized Recognition
| Task | Accuracy | F1-Score |
|------|----------|----------|
| Gender Recognition | **96%** | 0.96 |
| Pure Emotion Recognition | 63% | 0.63 |

**Performance Challenges:**
- Neutral emotion (F1=0.29)
- Sad emotion (F1=0.50)

## 💻 How to Run
1. Install dependencies:
```bash
pip install librosa tensorflow scikit-learn matplotlib
