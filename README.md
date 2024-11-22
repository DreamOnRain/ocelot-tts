# OCELOT TTS MODEL

Overworld Chinese E-Learning Online Teacher (OCELOT),
a gamified mobile platform designed to enhance language learning
through conversational practice. OCELOT focuses on pronunciation
and listening skills, employing a Mandarin Chinese Text-to-Speech
model, tonal phoneme-based Automatic Speech Recognition, and
semantic textual similarity models for backend feedback.

---
## 0. Install dependences:
  ```bash
    pip install -r requirements.txt
  ```
## 1. Datasets
  [AISHELL-3](https://www.aishelltech.com/aishell_3)
  [CSMSC](https://www.data-baker.com/open_source.html)
  [LJ SPEECH](https://keithito.com/LJ-Speech-Dataset/)
  [VCTK](https://datashare.ed.ac.uk/handle/10283/2651)
  [ESD](https://hltsingapore.github.io/ESD/)

---

## 2. Training

  CUDA_VISIBLE_DEVICES=1,2,3 python train_ms.py -c configs/chinese.json -m chinese
  CUDA_VISIBLE_DEVICES=1,2,3 python train_ms.py -c configs/english_emotion.json -m english_emotion

---

## 5. Inference

  python3 ocelot.py Chinese '请问酒店怎么去' 0 'happy' 1
  python3 ocelot.py English 'In order to approach people, you best learn how to greet them first' 0 'happy' 1
---

## 6. Evaluation
  python3 evluation.py
  python3 evluation_english.py

---

## Related Projects

For further details, visit the official [GPT-SoVITS GitHub Repository](https://github.com/RVC-Boss/GPT-SoVITS/tree/main?tab=readme-ov-file).