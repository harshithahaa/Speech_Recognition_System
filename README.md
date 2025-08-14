## SPEECH RECOGNITION SYSTEM

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: HARSHITHA V

*INTERN ID*: CT06DG2210

*DOMAIN*: Artificial Intelligence

*DURATION*: 6 WEEEKS

*MENTOR*: NEELA SANTOSH

## Project Overview
This project delivers a lightweight yet accurate automatic speech recognition (ASR) system that converts English speech from .wav audio files into written text. It uses the Wav2Vec2.0 Base 960h model developed by Facebook AI, integrated with PyTorch, torchaudio, and Hugging Face Transformers for a complete and efficient pipeline.

As speech becomes an increasingly dominant mode of communication—through podcasts, voice notes, interviews, and calls—organizations require reliable transcription tools. Commercial ASR APIs often come with privacy concerns, pricing limits, and internet dependencies. This offline system solves that by providing private, open-source transcription in real-time.

The application includes a command-line interface for local testing and is easily extensible to support web-based interfaces like Streamlit. Its modular design ensures clarity, ease of use, and scalability for future enhancements like multi-language support or real-time streaming.

## Tools & Technologies Used
Python:                             Main programming language
PyTorch:                          	Neural network framework to run the model
Hugging Face Transformers:         	Provides the Wav2Vec2 model and tokenizer
torchaudio:                       	Handles audio file loading, resampling, and waveform conversion
facebook/wav2vec2-base-960h:	      Pre-trained speech recognition model
venv (Virtual Environment):       	Isolates dependencies
WAV File Input:                   	Accepts .wav files for offline speech transcription

## How the Project Works (Architecture)
1. Audio Input
The user supplies a .wav audio file. Files are expected to be single-speaker and in English.

2. Preprocessing
The audio waveform is loaded using torchaudio. If stereo, it is converted to mono. The waveform is then resampled to the 16kHz rate required by Wav2Vec2.

3. Feature Extraction
The Hugging Face Wav2Vec2Processor normalizes the waveform and prepares it for inference by converting it to model-compatible format.

4. Model Inference
The Wav2Vec2ForCTC model processes the audio and returns logits, which represent probabilities for each character/token.

5. Decoding
The most probable token path is decoded using the processor’s batch_decode() function, producing the final transcription.

6. Output Display
The transcription is printed in the console or can be integrated into a dashboard (e.g., Streamlit app) for user interaction.

## Future Improvements
Enable real-time transcription using microphone input
Add punctuation and capitalization to transcripts
Create a simple web interface using Streamlit
Support additional languages with multilingual models
Deploy as an API for integration into other apps

## Output
Running the transcription script on a harvard.wav file:

![Image](https://github.com/user-attachments/assets/88a9cd1b-d8c2-4940-91f6-4eca4eb09e01)
