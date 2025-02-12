# Voice-Assistance
# Voice Assistant - Amura

## Overview
Amura is a virtual voice assistant capable of performing general tasks like opening websites and responding to voice queries using AI. It uses **Google Generative AI (Gemini API)** for intelligent responses, **speech recognition** for voice commands, and **Google Text-to-Speech (gTTS)** for voice output.

## Features
- Open commonly used websites (Google, YouTube, Facebook, etc.) via voice commands.
- Respond to user queries using AI-powered responses.
- Convert text responses into speech.
- Use speech recognition to interact with users.

## Tech Stack
- **Python**
- **SpeechRecognition** (for voice input)
- **Google Generative AI (Gemini API)** (for intelligent responses)
- **gTTS (Google Text-to-Speech)** (for voice output)
- **Pygame** (for playing generated speech)
- **Webbrowser** (for opening websites)

## Installation
### Prerequisites
Ensure you have Python installed (version 3.7+ recommended). Then install the required dependencies:
```sh
pip install openai speechrecognition webbrowser pyttsx3 google-generativeai gtts pygame requests
```

### Set Up API Key
You need a **Google Gemini API Key** for AI responses. Store it securely as an environment variable:
```sh
export GOOGLE_API_KEY='your_api_key_here'
```

For Windows (PowerShell):
```powershell
$env:GOOGLE_API_KEY='your_api_key_here'
```

## How to Run
1. Start the script by running:
   ```sh
   python assistant.py
   ```
2. The assistant will initialize and wait for the wake word **"Hello"**.
3. Once activated, speak a command (e.g., "Open Google").
4. Amura will process the command and respond accordingly.

## Supported Commands
- **"Open Google"** → Opens Google in a web browser.
- **"Open YouTube"** → Opens YouTube.
- **"Open Facebook"** → Opens Facebook.
- **"Open WhatsApp Web"** → Opens WhatsApp Web.
- **General Questions** → Amura will respond using AI.

## Known Issues & Fixes
- **Microphone Not Detected?** Run:
  ```sh
  python -m speech_recognition
  ```
  to check available microphones.
- **No Sound Output?** Ensure `pygame.mixer` is properly initialized before playing the response.

## Future Improvements
- Implement hotword detection for continuous listening.
- Improve response accuracy with more AI models.
- Add more voice-based automation features.

## License
This project is open-source and available under the MIT License.


