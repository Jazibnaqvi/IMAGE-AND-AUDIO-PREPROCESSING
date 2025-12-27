# IMAGE-AND-AUDIO-PREPROCESSING
📌 Overview

This repository contains two complete preprocessing workflows designed for fundamental machine learning tasks:

Image Preprocessing Pipeline using the CIFAR-10 dataset

Audio (Speech) Preprocessing Pipeline using librosa, numpy, and matplotlib

Both pipelines demonstrate how raw data is transformed into structured, model-ready features while visualizing and analyzing the effect of each preprocessing step.

Old data is messy. Models are picky. Preprocessing is the bridge.

📂 Project Structure
├── image_preprocessing.py
├── audio_preprocessing.py
└── README.md

🖼️ Image Preprocessing Pipeline (CIFAR-10)
📊 Dataset

CIFAR-10 (color images, 32×32)

Two images selected from the test set

🔄 Preprocessing Steps

Loading original RGB images

Resizing (32×32 → 64×64)

Grayscale conversion

Horizontal flipping

Rotation (30 degrees)

Normalization (pixel values scaled to [0, 1])

Bonus: Custom sharpening filter (kernel-based)

Each step is:

Applied to both images

Visualized side-by-side

Analyzed by printing image shape and pixel value range

📈 Output

Final processed images combined into a tensor of shape:

[batch_size, C, H, W]


Suitable for CNN-based models

🧠 Key Learning

Spatial transformations improve robustness

Normalization stabilizes training

Sharpening enhances edge-based features

🎙️ Audio Preprocessing Pipeline (Speech Data)
📊 Dataset

Two example audio samples loaded via librosa

Acts as a small speech dataset

🔄 Preprocessing Steps

Audio loading

Resampling to 16 kHz

Amplitude normalization

Silence trimming

Smoothing filter (noise reduction)

Bonus: Noise addition experiment

📉 Visualizations

Raw waveform vs processed waveform (side-by-side)

MFCC feature heatmaps displayed on a log scale

🎼 Feature Extraction

MFCCs (Mel-Frequency Cepstral Coefficients)

Final feature tensor shape:

[2, 13, T]


(where T is the time dimension)

🧠 Key Learning

Silence trimming removes non-informative data

MFCCs provide compact, perceptually meaningful speech features

Preprocessing reduces the impact of noise on extracted features

🧪 Bonus Experiments

Image: Custom sharpening kernel enhances edges

Audio: Noise injection shows how preprocessing improves robustness

These experiments highlight how preprocessing decisions directly affect data quality and model readiness.

🛠️ Requirements
Image Pipeline

Python 3

torch

torchvision

numpy

opencv-python

matplotlib

Audio Pipeline

Python 3

librosa

numpy

matplotlib

▶️ How to Run

Open Google Colab or a local Python environment

Run image_preprocessing.py for Question 1

Run audio_preprocessing.py for Question 2

Observe printed statistics and generated figures

🎯 Final Note

Preprocessing isn’t glamorous.
It doesn’t trend.
But it decides whether your model learns truth or noise.

These pipelines follow classical, proven techniques — the kind that survived time, hardware limits, and academic scrutiny — while staying fully compatible with modern ML workflows.

Build forward.
But don’t forget what already works.
