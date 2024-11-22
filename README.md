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
  ```bash
  CUDA_VISIBLE_DEVICES=1,2,3 python train_ms.py -c configs/chinese.json -m chinese
  ```
  ```bash
  CUDA_VISIBLE_DEVICES=1,2,3 python train_ms.py -c configs/english_emotion.json -m english_emotion
  ```

---

## 3. Preprocessing

  Use preprocessing.py and chinese.py to do preprocessing.
  Some logics is including in inference.
  
---

## 4. Inference
  Chinese Demo
  ```bash
  python3 ocelot.py Chinese '请问酒店怎么去' 0 'happy' 1
  ```
  English Demo
  ```bash
  python3 ocelot.py English 'In order to approach people, you best learn how to greet them first' 0 'happy' 1
  ```
---

## 5. Evaluation
  ```bash
  python3 evluation.py
  ```
  ```bash
  python3 evluation_english.py
  ```

---

## Refernece

> **Conditional Variational Autoencoder with Adversarial Learning for End-to-End Text-to-Speech**\
> Jaehyeon Kim, Jungil Kong, Juhee Son \
> Paper: [https://arxiv.org/abs/2312.00752](https://arxiv.org/abs/2106.06103)

```
@inproceedings{kim2021conditional,
  title={Conditional variational autoencoder with adversarial learning for end-to-end text-to-speech},
  author={Kim, Jaehyeon and Kong, Jungil and Son, Juhee},
  booktitle={International Conference on Machine Learning},
  pages={5530--5540},
  year={2021},
  organization={PMLR}
}
```
