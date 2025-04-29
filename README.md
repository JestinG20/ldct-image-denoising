# 🧠 LDCT Image Denoising Using WGAN

This project implements a **Wasserstein Generative Adversarial Network (WGAN)** to denoise **Low-Dose CT (LDCT)** images, improving their quality while preserving diagnostic content. It aims to reduce radiation exposure to patients by enhancing LDCT images to match the quality of normal-dose scans.

## 🗂️ Project Overview

The notebook includes the following stages:
- Loading and preprocessing CT image data
- Building and training a WGAN architecture for image-to-image translation
- Visualizing generated vs. ground-truth images
- Evaluating performance using image quality metrics

The architecture uses:
- A **generator** to produce denoised images from noisy inputs
- A **critic (discriminator)** that distinguishes between real and generated images using the Wasserstein loss

## 📁 Dataset

The dataset consists of **paired LDCT and Normal Dose CT (NDCT)** images and was obtained from the **Cancer Imaging Archive (TCIA)**. It includes thoracic CT scans and is widely used in LDCT enhancement research.

Each image pair comprises:
- An LDCT scan with noise due to reduced radiation exposure
- A corresponding NDCT scan as a high-quality ground truth

## 🎯 Objectives

- Train a WGAN model that learns the mapping from noisy LDCT images to clean NDCT-like images.
- Minimize image artifacts while retaining diagnostic features.
- Evaluate image enhancement through visual inspection and quantitative analysis.

## 🧪 Key Features

- Custom WGAN implementation with gradient penalty (WGAN-GP)
- Data handling for 2D medical image slices
- Loss tracking and image generation throughout training
- Image quality metrics such as PSNR and SSIM for performance validation

## 📷 Visualizations

The notebook includes:
- Sample LDCT and NDCT image pairs
- Output of the generator vs. ground truth
- Loss curves for generator and critic
- Metric plots (if applicable)

These visualizations help assess how well the model improves image quality over time.

## 🙌 Acknowledgments

- Dataset sourced from the [Cancer Imaging Archive (TCIA)](https://www.cancerimagingarchive.net/).
- This project is inspired by recent work on deep learning–based low-dose CT enhancement using adversarial methods.
