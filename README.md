# SAVD: Sentiment-Aware Audio-Enhancement for Emotionally Engaging Visual Dialog

The full code will be released later.

We have opened 50 emotion-aware dialog and speech samples, which can be obtained from the dialog_data1.csv file for the emotional labels of the dialog samples with the full dialog, and from the speech folder for the corresponding speech samples.

![image](https://github.com/user-attachments/assets/ea7eb5f3-7c9d-4d11-ba3c-07726d0058e7)


 SAVD consists of two key modules: (i) a data augmentation module that adds sentiment-aware acoustic dialogues and generated image captions, and (ii) a unified temporal dialogue modeling module that learns the dependence of triple modalities (language, vision, audio) and builds three warm-up tasks for cross-modal interactions.


Preprocess datasets

image_chat：https://parl.ai/projects/image_chat/

Audio: We adopt Parler-TTS (https://github.com/huggingface/parler-tts) that can generate sentiment-aware audio for a given text by introducing an emotional style in the prompt

Caption: We employ a large vision-language model (LVLM), BLIP-2 OPT (6.7B), to generate the textual caption for visual image.

UTTDM Warm up and Fine-tuning

UTTDM module that represents the tri-modal dependency on language, vision and audio in temporal dialogue flow and incorporates three warm-up tasks: image and caption alignment (ICA), cross-modal contrastive learning (CCL), and next utterance prediction (NUP).

![image](https://github.com/user-attachments/assets/4669a6e8-c1cc-4aac-91b8-3503aa42c376)



Main Results

![image](https://github.com/user-attachments/assets/a0fa4ac0-f087-45b4-b8a1-d919640e32ac)
