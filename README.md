# Making Visual Dialogue More Engaging: A New Task, Method, and Metric



We have opened 50 emotion-aware dialog and speech samples, which can be obtained from the dialog_data1.csv file for the emotional labels of the dialog samples with the full dialog, and from the speech folder for the corresponding speech samples.
![image](https://github.com/user-attachments/assets/875e7365-3f0b-4a49-80b0-ba41de2b910b)

 SAVD consists of two key modules: (i) a data augmentation module that adds sentiment-aware acoustic dialogues and generated image captions, and (ii) a unified temporal dialogue modeling module that learns the dependence of triple modalities (language, vision, audio) and builds three warm-up tasks for cross-modal interactions.

 
<img width="1860" height="850" alt="image" src="https://github.com/user-attachments/assets/094791ca-cf34-438e-b19d-ec10637f3a37" />




Preprocess datasets

image_chat：https://parl.ai/projects/image_chat/

Audio: We adopt Parler-TTS (https://github.com/huggingface/parler-tts) that can generate sentiment-aware audio for a given text by introducing an emotional style in the prompt

Caption: We employ a large vision-language model (LVLM), BLIP-2 OPT (6.7B), to generate the textual caption for visual image.

UTTDM Warm up and Fine-tuning

UTTDM module that represents the tri-modal dependency on language, vision and audio in temporal dialogue flow and incorporates three warm-up tasks: image and caption alignment (ICA), cross-modal contrastive learning (CCL), and next utterance prediction (NUP).

![image](https://github.com/user-attachments/assets/9b6ddd2c-65d1-4808-be4b-48265ab498fb)



Main Results:

![image](https://github.com/user-attachments/assets/61cc38cb-9170-4ed3-b5af-4775345cff84)


MME Metric:


![image](https://github.com/user-attachments/assets/d6ef9f4c-9c21-42fd-8bdd-b9fb11f01648)


