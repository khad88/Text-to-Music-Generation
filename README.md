#Text-to-Music Generation: A Survey and Project Proposal

## Overview

This repository presents a comprehensive survey of **Text-to-Music Generation**, one of the emerging research directions in Generative AI.

The project reviews the evolution of text-conditioned music generation models, analyzes state-of-the-art architectures, discusses prompt engineering techniques, benchmark datasets, evaluation metrics, and proposes a practical research direction for adapting modern open-source foundation models to generate **Vietnamese traditional music** using efficient fine-tuning methods.

---

## Objectives

* Understand the development of Text-to-Music Generation.
* Compare recent foundation models from 2023–2026.
* Analyze datasets and evaluation metrics.
* Study Prompt Engineering and Retrieval-Augmented Generation (RAG).
* Identify current research gaps.
* Propose a feasible implementation based on PEFT/LoRA.

---

## Contents

```
1. Introduction to Text-to-Music Generation
2. Evolution of Music Generation Models
3. State-of-the-art Models
4. Prompt Engineering
5. Public Datasets
6. Evaluation Metrics
7. Research Gaps
8. Proposed Project
```

---

## Evolution of Text-to-Music

The survey summarizes four major generations of AI music generation:

| Stage                  | Representation  | Main Technique              |
| ---------------------- | --------------- | --------------------------- |
| Symbolic               | MIDI / MusicXML | Transformer                 |
| Spectrogram            | Mel Spectrogram | CNN / Diffusion             |
| Deep Audio Compression | EnCodec + RVQ   | Autoregressive Transformer  |
| Latent Diffusion       | Latent Audio    | Diffusion Transformer (DiT) |

---

## Reviewed Models

The report covers several representative models:

| Model             | Year      | Highlights                           |
| ----------------- | --------- | ------------------------------------ |
| MusicGen          | 2023      | Fast autoregressive music generation |
| Stable Audio Open | 2024      | DiT-based diffusion model            |
| LeVo              | 2025      | High-quality singing generation      |
| ACE-Step          | 2025/2026 | Hybrid diffusion + autoregressive    |
| AudioX            | 2026      | Anything-to-Audio framework          |
| Stable Audio 3.0  | 2026      | Long-form music generation & editing |

---

## Prompt Engineering

The project discusses effective prompt construction for music generation, including:

* Genre
* Tempo
* Instrumentation
* Song structure
* Mood
* Style

It also introduces **Retrieval-Augmented Generation (RAG)** to automatically rewrite user prompts into expert-level music descriptions.

---

## Datasets

The following datasets are reviewed:

* MusicCaps
* MTG-Jamendo
* IF-caps

These datasets provide audio-caption pairs, music tags, and multimodal annotations for training and evaluation.

---

## Evaluation

### Objective Metrics

* Fréchet Audio Distance (FAD)
* Kernel Audio Distance (KAD)
* CLAP Score

### Subjective Metrics

* Mean Opinion Score (MOS)
* Pairwise Human Preference

---

## Proposed Research Direction

Instead of training a Text-to-Music model from scratch, this project proposes:

> Fine-tuning an open-source foundation model using **PEFT/LoRA** to generate Vietnamese traditional music.

Target characteristics include:

* Vietnamese traditional instruments
* Folk melodies
* Traditional rhythm patterns
* Cultural music styles

Potential backbone models:

* Stable Audio 3.0 Small
* ACE-Step

---

## Proposed Pipeline

```
Audio Collection
        │
        ▼
Caption Generation
(LLM / Pseudo-labeling)
        │
        ▼
Foundation Model
(Stable Audio 3.0 / ACE-Step)
        │
        ▼
LoRA Fine-tuning
        │
        ▼
Prompt Engineering (RAG)
        │
        ▼
Evaluation
(FAD, KAD, CLAP, MOS)
```

---

## Technologies

* Python
* PyTorch
* HuggingFace
* PEFT / LoRA
* Diffusion Transformer
* CLAP
* EnCodec
* RAG
* Large Language Models

---

## Future Work

* Build a Vietnamese traditional music dataset.
* Fine-tune open-source Text-to-Music models.
* Improve prompt rewriting using RAG.
* Explore multimodal conditioning (video + music).
* Support long-form music generation.

---

## References

The survey is based on recent research papers including:

* MusicLM
* MusicGen
* Stable Audio Open
* LeVo
* ACE-Step
* AudioX
* Stable Audio 3.0
* AudioLDM
* MTG-Jamendo
* MusicCaps

---

## Authors

* Doãn Đăng Khoa
* Nguyễn Minh Sáng

Faculty of Information Technology 1
Posts and Telecommunications Institute of Technology (PTIT)

2026
