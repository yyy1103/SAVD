# Making Visual Dialogue More Engaging: A New Task, Method, and Metric

The full code will be released later.

We have opened 50 emotion-aware dialog and speech samples, which can be obtained from the dialog_data1.csv file for the emotional labels of the dialog samples with the full dialog, and from the speech folder for the corresponding speech samples.
![image](https://github.com/user-attachments/assets/875e7365-3f0b-4a49-80b0-ba41de2b910b)

![image](https://github.com/user-attachments/assets/901c90ad-75b3-49fb-8f8b-39341da5bad1)

![image](https://github.com/user-attachments/assets/4cdaba91-8f49-4713-9014-7d3c1a2e43dd)



 SAVD consists of two key modules: (i) a data augmentation module that adds sentiment-aware acoustic dialogues and generated image captions, and (ii) a unified temporal dialogue modeling module that learns the dependence of triple modalities (language, vision, audio) and builds three warm-up tasks for cross-modal interactions.


Preprocess datasets

image_chat：https://parl.ai/projects/image_chat/

Audio: We adopt Parler-TTS (https://github.com/huggingface/parler-tts) that can generate sentiment-aware audio for a given text by introducing an emotional style in the prompt

Caption: We employ a large vision-language model (LVLM), BLIP-2 OPT (6.7B), to generate the textual caption for visual image.

UTTDM Warm up and Fine-tuning

UTTDM module that represents the tri-modal dependency on language, vision and audio in temporal dialogue flow and incorporates three warm-up tasks: image and caption alignment (ICA), cross-modal contrastive learning (CCL), and next utterance prediction (NUP).

![image](https://github.com/user-attachments/assets/4669a6e8-c1cc-4aac-91b8-3503aa42c376)



Main Results

![image](https://github.com/user-attachments/assets/61cc38cb-9170-4ed3-b5af-4775345cff84)

