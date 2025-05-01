# Next Utterance Prediction for Mental Health Counseling

This project explores the task of predicting the next utterance in therapeutic conversations using transformer-based language models. Designed to assist mental health platforms and counselors, the system focuses on generating emotionally intelligent and contextually relevant responses in sensitive dialogue settings.

## Team
- Aahan Piplani (2022001)
- Akshat Karnwal (2022052)
- Kartikeya (2022247)

## Project Overview

We propose a two-stage modular pipeline for next utterance prediction:
1. **Candidate Generation** — Generates multiple possible responses for a given conversational context.
2. **Re-ranking Module** — Selects the most semantically appropriate response using a BERT-based scoring model inspired by reinforcement learning principles.

### Key Highlights
- **Reinforcement-Inspired Selection**: The BERT-based re-ranker is trained to act like a value function, assigning scores to generated candidates based on semantic alignment with ground-truth responses.
- **Transformer Backbones**: Used pre-trained language models like DialoGPT and T5 for candidate generation.
- **Evaluation Metrics**: Performance is measured using BLEU and BERTScore (F1 = 0.8423).

## Architecture
```text
Input Dialogue History
│ 
▼ 
Candidate Generator (DialoGPT / T5)
│ 
Top-k Responses
│ 
▼ 
BERT-based Re-ranker
│ 
▼ 
Final Selected Response


```
## Results

| Model              | BLEU Score | BERTScore (F1) |
|--------------------|------------|------------------|
| T5-small           | 0.0162     | 0.8431           |
| DialoGPT-medium    | 0.0240     | 0.9500           |
| Re-ranked Pipeline | 0.0250     | 0.8423           |

## Report

*   Project Report (PDF)

## Setup Instructions

Clone the repository:
```bash
git clone https://github.com/Aahan22001IIITD/NLP---project
cd NLP---project
