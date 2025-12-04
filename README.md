# How to build a FREE Text-to-Speech AI App on Google Colab using Pinggy

A modern, high-quality **Text-to-Speech (TTS)** interface powered by **Kokoro ONNX**.
This project provides an elegant Gradio web interface for generating natural-sounding speech in multiple languages, and can be self-hosted online using **Pinggy**.


## Features

* High-quality neural speech generation
* Multi-language support (English, Japanese, Chinese, Spanish, etc.)
* Multiple natural-sounding voices
* Adjustable speech speed
* Clean, modern Gradio UI
* Instant audio preview + WAV export
* Free public hosting using **Pinggy**
* Runs on Google Colab, local machine, or any cloud server


## Clone the Repository

Clone the official repository:

```bash
git clone https://github.com/vpakarinen/kokoro-tts-webui.git
cd kokoro-tts-webui
```



## Installation

Install all required dependencies:

```bash
pip install -r requirements.txt
```

or manually install:

```bash
pip install gradio kokoro-onnx soundfile torch numpy
```

# Self-Hosting the App Using Pinggy 

Pinggy allows you to expose your local Kokoro TTS WebUI publicly on the Internet.

### **Step 1 — Run the WebUI**

Start the app normally:

```bash
python app.py
```

The app runs at:

```
http://localhost:8000
```

### **Step 2 — Open a Pinggy tunnel**

Install Pinggy:
```
!pip install pinggy

```
Create the Pinggy Tunnel:

```bash
import pinggy
tunnel1 = pinggy.start_tunnel(
 forwardto="localhost:8000",
)
print(f"Tunnel1 started - URLs: {tunnel1.urls}")
```

Pinggy will generate a public HTTPS URL like:

```
https://blue-cobra-1234.a.pinggy.link
```

Share this link with anyone - your TTS WebUI is now globally accessible!
## Screenshot


![app](https://github.com/Bidisha314/TTS_application/blob/main/app.jpg)


## Project Structure

```
├── app.py                # Main Gradio WebUI script
├── README.md             # Documentation
├── requirements.txt      # Dependencies
├── assets/               # Screenshots/images
└── models/               # Kokoro model files (auto-downloaded)
```



## Usage

1. Enter the text you want to convert into speech
2. Select a voice
3. Select a language
4. Adjust speaking speed
5. Click **Generate Speech**
6. Listen or download the audio

Simple and fast.


## 🛠️ Built With

* **Kokoro ONNX**
* **Gradio**
* **Python 3.9+**
* **NumPy**
* **SoundFile**
* **Torch**
* **Pinggy (self-hosting)**


