## 😄 Emotion Recognition from Facial Expressions and Voice Tone
## 📝 Introduction
This project focuses on recognizing emotions from facial expressions in images and voice tone in audio files. It uses OpenCV for facial emotion detection, Whisper for speech recognition, and machine learning models for voice emotion classification. The goal is to demonstrate how computer vision and audio analysis can be integrated to create an emotion-aware system.

This project was developed using Google Colab for easy setup and execution.

## ⚙️ How the Project Works
## 🖼️ Face Emotion Detection
## Face Detection:
Uses OpenCV’s Haar cascade classifier to detect faces in an image.

## Emotion Classification:
A pre-trained mini XCEPTION model is used to classify the detected face's emotion into one of these categories: Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral.

## 🎤 Voice Emotion Detection
## Audio Preprocessing:
Extracts MFCC (Mel-frequency cepstral coefficients) and pitch features from the uploaded audio file using Librosa.

## Emotion Classification: 
A dummy classifier is used to classify the emotion (happy, sad, angry, neutral) based on the extracted features.

## Speech Recognition: 
Whisper transcribes the audio to text and detects the language used in the speech.

## 🔧 Installation & Setup
Before running the code, you need to install the necessary dependencies:

## Install Dependencies
!pip install -q keras opencv-python librosa moviepy openai-whisper pydub ffmpeg-python
## Download Pre-trained Model
bash
Copy
Edit
!wget -q https://github.com/oarriaga/face_classification/raw/master/trained_models/emotion_models/fer2013_mini_XCEPTION.102-0.66.hdf5 -O emotion_model.h5
⚡ Running the Project in Google Colab
Open the notebook in Google Colab.

Install dependencies and download the pre-trained face emotion model.

Upload either:

An image file to detect facial emotions, or

An audio file (MP3, MP4, WAV, or other supported formats) to detect voice emotions and transcribe the speech.

The code will automatically run, and you will get:

Detected facial emotion from the image (if an image is uploaded).

Detected voice emotion and transcription (if an audio file is uploaded).

## 🧰 Technologies Used
Python

OpenCV: Used for detecting faces in images.

Keras: For loading the pre-trained emotion detection model.

Whisper: OpenAI’s model for automatic speech recognition (ASR).

Librosa: For audio feature extraction (MFCC, pitch).

pydub: To convert audio files to WAV format for consistent processing.

SVC (Support Vector Classifier): Used for training and classifying voice emotions.

## 🧑‍💻 How It Works
## 1. Face Emotion Detection:
The uploaded image is processed to detect faces using Haar cascade.

A mini XCEPTION model (pre-trained on the FER-2013 dataset) is used to classify the emotion of the face in the image.

The emotion is displayed on the image with a bounding box around the face.

## 2. Voice Emotion Detection:
Audio is pre-processed to extract MFCC and pitch features.

The extracted features are classified using a dummy SVC model.

The audio is transcribed to text using Whisper, and the detected emotion and language of the audio are displayed.

## 3. Universal Audio Converter:
If an audio file is uploaded in any format other than WAV, it is converted to WAV using pydub for consistent processing.

## 💻 Sample Output
When uploading an image:
🎭 Detecting Facial Emotion...
Facial Emotion Detected: Happy
When uploading an audio file:
🎤 Detecting Voice Emotion...
Voice Emotion Detected: Happy
Speech Transcription: I am feeling great today!
Language Detected: en
## 🏁 Conclusion
This project demonstrates how to recognize emotions from both facial expressions and voice tone using computer vision and audio processing. It uses advanced models like Whisper for speech recognition and a pre-trained neural network for facial emotion detection, making it a useful tool for emotion-aware applications.

The integration of face and voice emotion detection makes this project versatile, with potential applications in security systems, customer feedback analysis, virtual assistants, and more.
