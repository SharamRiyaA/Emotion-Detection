
# 😄 Emotion Recognition from Facial Expressions and Voice Tone

## 📝 Introduction

This project detects emotions from both facial expressions (images) and voice tone (audio). It uses OpenCV for facial detection, a pre-trained deep learning model for emotion classification, Whisper for speech transcription, and audio feature extraction for voice emotion detection.

---

## ⚙️ How the Project Works

### 🖼️ Facial Emotion Detection
- Detects faces using Haar Cascade (OpenCV).
- Classifies emotions using a pre-trained mini XCEPTION model.
- Emotion categories: Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral.

### 🎤 Voice Emotion Detection
- Extracts MFCC and pitch features using Librosa.
- Dummy classifier (SVM) predicts voice emotion: happy, sad, angry, or neutral.
- Transcribes audio to text and detects language using Whisper.

---

## 🔧 Installation & Setup

### Install Dependencies
```bash
!pip install -q keras opencv-python librosa moviepy openai-whisper pydub ffmpeg-python
```

### Download Pre-trained Model
```bash
!wget -q https://github.com/oarriaga/face_classification/raw/master/trained_models/emotion_models/fer2013_mini_XCEPTION.102-0.66.hdf5 -O emotion_model.h5
```

---

## ⚡ How to Use

1. Run the notebook in Google Colab.
2. Install the dependencies and download the model.
3. Upload:
   - An image file (.jpg/.png) → to detect **facial emotion**.
   - An audio file (.mp3/.wav/.mp4/etc) → to detect **voice emotion** and get **speech transcription**.
4. The script will automatically process the uploaded files and print the detected emotions and transcription.

---

## 🧰 Tools Used

- Python
- OpenCV
- Keras
- Whisper (by OpenAI)
- Librosa
- Pydub
- scikit-learn (SVM Classifier)

---

## 🧪 Output Example

### Image Input:
```
🎭 Detecting Facial Emotion...
Facial Emotion Detected: Happy
```

### Audio Input:
```
🎤 Detecting Voice Emotion...
Voice Emotion Detected: Sad
Speech Transcription: I'm not feeling well today.
Language Detected: en
```

---

## 📌 Notes

- The voice emotion classifier is a dummy model for demonstration purposes.
- Whisper transcribes audio accurately and detects the spoken language.
- Works best with clear frontal face images and audio without background noise.

---

## ✅ Future Improvements

- Train a real voice emotion classifier with labeled emotional audio datasets.
- Add multi-face detection and support for video inputs.
- Improve UI and integrate with web apps for real-time emotion analysis.

---
