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

## Model Improvements
One recurrent problem with our model is that it often confuses Swedish for Norwegian. To mitigate this problem and to improve accuracy, we present some potential improvements that can be made.

### Data-centric approach
In our data-centric approach, we initially started from an English language Whisper checkpoint. We then trained the model as usual with the Swedish data from the Common Voice dataset. However, we found that this approach significantly worsened the performance. The transcriptions were more biased towards the English language, resulting in outputs that resembled "Swenglish."

One way to improve model performance is to increase the amount of training data [[1](https://machinelearningmastery.com/improve-deep-learning-performance/), [2](https://iopscience.iop.org/article/10.1088/1742-6596/1168/2/022022/pdf)]. Increasing the training size is especially useful for complicated models, for instance, DNNs. Using a larger dataset means that we can obtain a more diverse range of samples. Having diverse data helps the model generalize better to unseen data, and we reduce the chance of overfitting.

The National Library of Norway offers data suitable for Automatic Speech Recognition (ASR). The data is available at: [NST Swedish ASR Database (16 kHz)](https://www.nb.no/sprakbanken/en/resource-catalogue/oai-nb-no-sbr-56/). The dataset contains 124.2 GB of speech recordings in Swedish. Currently, our model is only trained on 7.41k rows of data, while the NST dataset consists of over 300k rows of data. Only selecting a subset of the NST dataset for training could potentially increase the accuracy of our model. However, the downside of increasing the training data size is that it would take longer to train.

### Model-centric approach
For a model-centric approach to fine-tuning Whisper for a specific language like Swedish, several strategies can be 
considered. These include adjusting learning rates, and experimenting with batch sizes. However, we were unable to test 
and validate a model-centric approach within the timeframe of our project.

```
