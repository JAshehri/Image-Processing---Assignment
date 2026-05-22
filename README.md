# Image Denoising and Quality Enhancement

This repository contains the official implementation and documentation for the Digital Image Processing project, focusing on spatial and frequency domain image restoration techniques.

## Repository Structure
* **`dataset/`**: Contains the core benchmarking images used for evaluation (*camera, coins, text, rice, astronaut*).
* **`Image_Denoising_and_Enhancement.ipynb`**: The complete Jupyter Notebook containing the Python implementation for automated dynamic optimization, filtering configurations, and visual panel outputs.
* **`Image_Denoising_and_Quality_Enhancement_Report.pdf`**: The final comprehensive project report outlining noise identification, engineering rationales, mathematical metrics (PSNR/SSIM), and benchmarking analyses.

## Methods Evaluated
* **Spatial Domain:** Median Filter, Gaussian Filter, Mean Filter, and Bilateral Filter.
* **Frequency Domain:** Gaussian Low-Pass Filter (GLPF).

## Key Results
* **Spatial Domain Average:** PSNR = 28.46 dB | SSIM = 0.8019 (Optimal Performance)
* **Frequency Domain Average:** PSNR = 24.10 dB | SSIM = 0.6273
