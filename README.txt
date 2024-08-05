LINK TO APP DEMO: https://youtu.be/PYmgFxYyTkQ

# Interview Insight Generator

This Colab notebook contains a Streamlit app that transcribes audio and video interviews, generates insights, and answers follow-up questions using AI.

## Features

1. Audio/Video Transcription: Converts uploaded audio or video files into text using OpenAI's Whisper model.
2. Insight Generation: Analyzes the transcription to provide key insights using a BART language model.
3. Follow-up Questions: Allows users to ask questions about the transcribed content and receive AI-generated answers.

## Setup

1. Run the first cell to install required packages:
   - openai-whisper
   - moviepy
   - streamlit
   - pyngrok
   - transformers
   - torch

2. The second cell contains the main application code (`app.py`).

3. Set up ngrok for tunneling:
   - Run the cell to set the ngrok authtoken
   - Set the NGROK_AUTHTOKEN environment variable

4. Launch the Streamlit app and create an ngrok tunnel to make it accessible.

## Usage

1. Upload an audio or video file (supported formats: wav, mp3, m4a, mp4, avi, mov, mkv).
2. The app will transcribe the file and display the transcription.
3. Choose insight generation options:
   - Insight type (general, technical, business)
   - Number of insights
   - Content type (e.g., interview, presentation)
4. Generate insights based on the transcription.
5. Ask follow-up questions about the content.

## Components

- `convert_to_audio()`: Converts video files to audio if necessary.
- `transcribe_audio()`: Uses Whisper model to transcribe audio to text.
- `generate_response()`: Generates responses using the BART model.
- `generate_insights()`: Extracts and formats insights from the transcription.
- `answer_followup()`: Generates answers to follow-up questions.

## Deployment

The notebook uses ngrok to create a public URL for the Streamlit app running in Colab. This allows for temporary deployment and sharing of the app.

## Notes

- This setup is suitable for testing and demonstrations, not for permanent deployment.
- The ngrok free tier has limitations on simultaneous sessions.
- Colab has usage limits and may disconnect after periods of inactivity.

## Creators

Created by Ama Annor and Claude Quartey