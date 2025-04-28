# SPEECH-RECOGNITION-SYSTEM
COMPANY:CODE TECH IT SOLUTIONS

NAME:VENNAM AISHWARYA

INTERN ID: CT04WT94

DOMAIN:ARTIFICIAL INTELLIGENT

DURATION:4 WEEKS

This Python script demonstrates a basic speech recognition system using the speech_recognition library, which allows the program to capture audio input from a microphone and convert it into text. Here’s a 

detailed breakdown of its functionality:

1. Initialization

The script begins by importing the speech_recognition library (commonly referred to as sr for brevity). This library provides tools for interacting with audio input sources, such as microphones, and supports 

multiple speech recognition APIs, including Google's Web Speech API. The Recognizer class is initialized as recognizer, which will handle the audio processing and recognition tasks.

2. Audio Capture

The script uses a context manager (with sr.Microphone() as source) to access the default system microphone. This ensures proper resource management, automatically handling microphone setup and release. Once the 

microphone is active, the program prints "Listening..." to indicate it is ready to capture audio.

The recognizer.listen(source) method records audio from the microphone until it detects a pause (or silence), storing the recorded audio in audio_data. This step is crucial for real-time speech recognition, as it

waits for user input before proceeding.

3. Speech Recognition
  
4.After capturing audio, the script attempts to transcribe it into text using Google's free Web Speech API (recognize_google()). This API processes the audio data and returns the recognized speech as a string. 

The "Recognizing..." message indicates that the conversion is in progress.

5. Error Handling
 
6.The script includes two key exception handlers:

UnknownValueError: Triggered when the audio is unclear or unintelligible, resulting in the message "Sorry, I could not understand the audio."

RequestError: Occurs if there is a problem with the API request (e.g., no internet connection or server issues), displaying an error message with details.

5. Output

6.If successful, the recognized text is printed as "You said: [text]". This provides immediate feedback, making the script useful for voice-controlled applications, voice assistants, or accessibility tools.

Key Features & Limitations

Real-time Processing: Captures and processes speech dynamically.

Dependency on Google API: Requires an internet connection and relies on external services.

Basic Error Handling: Covers common issues but lacks advanced recovery mechanisms.

This script serves as a foundation for more complex voice-interactive systems, such as voice commands, transcription tools, or AI assistants. Further enhancements could include offline recognition (using CMU 

Sphinx) or integrating additional NLP functionalities.
