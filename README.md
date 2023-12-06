# Whisper-Small-SV: Fine-Tuned Whisper Model for Swedish

Welcome to the repository for Whisper-Small-SV, a specialized version of the Whisper model fine-tuned for Swedish 
language processing. Our goal is to provide a robust and efficient model for transcribing Swedish audio, with a 
particular focus on YouTube video content.

## About the Model

The Whisper-Small-SV is a fine-tuned version of OpenAI's Whisper model, specifically adapted for the Swedish language.

For more information about the model, visit: [Hugging Face Model Page](https://huggingface.co/GroupSix/whisper-small-sv)

## Hugging Face App

We have developed an application that utilizes the Whisper-Small-SV model for transcribing audio directly from YouTube 
videos. The app is hosted on Hugging Face Spaces, providing an easy-to-use interface for real-time transcription.

**Access the App Here:** [Hugging Face Spaces App](https://huggingface.co/spaces/GroupSix/language)

### How to Use the App

1. Navigate to the app link above.
2. Input the URL of the YouTube video you want to transcribe.
3. The app will process the audio and provide you with the transcribed text in Swedish.

### Updating the Language App

To contribute or update the language app, you can push changes to the Hugging Face repository using the following 
script:

```bash
./push_hugging_face_language.sh
```