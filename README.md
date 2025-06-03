
# 🤟 Real-Time Indian Sign Language (ISL) to Text & Speech Translator

A real-time gesture recognition system that translates Indian Sign Language (ISL) to both text and speech using a CNN-LSTM model, MediaPipe, and a web-based UI.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Features](#features)
- [System Architecture](#system-architecture)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Evaluation Metrics](#evaluation-metrics)
- [Limitations](#limitations)
- [Roadmap](#roadmap)
- [Team](#team)
- [License](#license)

---

## 📘 Project Overview

This project bridges the communication gap between hearing-impaired individuals and the general population. It recognizes dynamic ISL hand gestures in real-time using a webcam and displays the corresponding text and speech output through a responsive browser interface.

---

## ❓ Problem Statement

Many ISL users face communication barriers due to the lack of widespread understanding of sign language. Existing systems often support only static gestures or require expensive sensor-based hardware. We aim to create a cost-effective, real-time ISL interpreter using only a webcam and deep learning.

---

## 🚀 Features

### Feature 1: Real-Time ISL to Speech
- Captures and classifies dynamic ISL gestures
- Outputs both text and voice in real-time
- Enables natural conversation flow

### Feature 2: Speech to ISL Gesture (Optional Extension)
- Converts voice to text using NLP
- Matches words to ISL animations
- Visualizes gestures for non-verbal feedback

---

## 🧠 System Architecture

```text
Webcam Input → MediaPipe Landmark Extraction → CNN-LSTM Model → Text Output → TTS Engine (for speech)
````

---

## 📂 Dataset

* Public ISL dataset or custom hand gesture videos
* MediaPipe used to extract 21 hand landmarks per frame
* Input shape: `(30 frames, 21 landmarks, 3 coordinates)`

---

## 🧬 Model Architecture

* **CNN Layers:** Extract spatial hand features from each frame
* **LSTM Layers:** Model gesture sequences over time
* **Dense Layers + Softmax:** Output class probabilities

---

## 🧰 Technologies Used

* **Python, TensorFlow, Keras**
* **MediaPipe** for hand tracking
* **Flask** for backend API
* **Bolt** for interactive frontend UI
* **TensorFlow\.js** for browser deployment
* **Google Text-to-Speech (TTS)**

---

## 🛠️ Installation

```bash
git clone https://github.com/yourusername/isl-translator.git
cd isl-translator
pip install -r requirements.txt
python app.py
```

For the frontend, use Bolt or any frontend tool to interact with `/predict` API and display results in real-time.

---

## ▶️ Usage

1. Run `app.py` to start the Flask server
2. Open your browser to the Bolt frontend interface
3. Show hand gestures to the webcam
4. View translated text and hear speech output

---

## 📈 Evaluation Metrics

* **Accuracy:** \~90% on test data
* **F1-Score:** Estimated 0.85–0.90
* **AUC-ROC:** Estimated 0.90–0.95
* **Latency:** <300ms per prediction

---

## ⚠️ Limitations

* Model performance may drop in poor lighting or occluded hand positions
* Limited vocabulary (only trained classes recognized)
* Dataset size and quality affect robustness
* Speech-to-sign is based on keyword matching, not full grammar parsing

---

## 🗺️ Roadmap

### Q1:

* Literature Survey
* Data Gathering & Preprocessing

### Q2:

* Model Design & Training (CNN + LSTM)
* Backend API with Flask

### Q3:

* Real-time Frontend using Bolt
* Voice Output Integration
* Testing and Deployment

---

## 👨‍💻 Team

* **Mayur M.** - Model Development, UI
* **\[Teammate 2]** - Dataset Handling, Preprocessing
* **\[Teammate 3]** - Backend API, Deployment
* **Guide:** Prof. \[Faculty Name]

---

## 📄 License

This project is licensed under the MIT License. Feel free to reuse with credit.

---

## 🌐 Acknowledgements

* [Google MediaPipe](https://mediapipe.dev/)
* [TensorFlow](https://www.tensorflow.org/)
* [Flask](https://flask.palletsprojects.com/)

```

Let me know if you'd like this exported as a downloadable `.md` file.
```
