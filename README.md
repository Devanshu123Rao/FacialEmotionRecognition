# FacialEmotionRecognition

Facial Emotion Recognition Using Transfer Learning and Stable Diffusion

A deep learning project for facial emotion recognition using transfer learning with a Vision Transformer (ViT)-based facial emotion recognition model. To improve the diversity of the training data, Stable Diffusion was used to generate additional synthetic facial images representing different emotional expressions.

The generated images were combined with real facial images and used to fine-tune the Hardly Human facial emotion recognition model, which is based on a fine-tuned Vision Transformer architecture.

📌 Project Overview

Facial Emotion Recognition (FER) is a computer vision task that aims to identify human emotions from facial expressions.

In this project, I explored a transfer learning-based approach where an existing Vision Transformer-based facial emotion recognition model was further fine-tuned using a combination of:

Real facial emotion images
Synthetic facial images generated using Stable Diffusion

The primary motivation for using synthetic images was to increase the diversity of the training dataset and provide additional examples of different facial expressions.

Overall Pipeline
                 ┌─────────────────────┐
                 │   Real Face Images  │
                 └──────────┬──────────┘
                            │
                            │
                            ▼
                 ┌─────────────────────┐
                 │   Emotion Dataset   │
                 └──────────┬──────────┘
                            │
                            │
                            │
       ┌────────────────────┴────────────────────┐
       │                                         │
       ▼                                         ▼
┌──────────────────┐                  ┌─────────────────────┐
│ Real Images      │                  │ Stable Diffusion    │
│                  │                  │ Generated Images    │
└────────┬─────────┘                  └──────────┬──────────┘
         │                                       │
         └──────────────────┬────────────────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Combined Dataset    │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Vision Transformer │
                 │ Emotion Model       │
                 └──────────┬──────────┘
                            │
                            │ Fine-tuning
                            ▼
                 ┌─────────────────────┐
                 │ Fine-tuned FER      │
                 │ Model               │
                 └──────────┬──────────┘
                            │
                            ▼
                 ┌─────────────────────┐
                 │ Emotion Prediction  │
                 └─────────────────────┘
