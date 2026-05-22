# Image Denoising and Quality Enhancement

This repository contains the official implementation, benchmarking suite, and documentation for the Digital Image Processing project, focusing on adaptive spatial and frequency domain image restoration techniques.

## Repository Structure

*   `dataset/`: Contains the core benchmarking images used for evaluation (`camera`, `coins`, `text`, `rice`, `astronaut`).
*   `Image_Denoising_and_Enhancement.ipynb`: The complete Jupyter Notebook containing the Python implementation for automated dynamic optimization, filtering configurations, and visual panel outputs.
*   `Image_Denoising_and_Quality_Enhancement_Report.pdf`: The final comprehensive project report outlining noise identification, engineering rationales, mathematical metrics (PSNR/SSIM), and benchmarking analyses.

## Methods Evaluated

*   **Spatial Domain:** Median Filter, Gaussian Filter, Mean Filter, and Bilateral Filter (optimized across $3\times3$, $5\times5$, and $7\times7$ window topologies).
*   **Frequency Domain:** Global Gaussian Low-Pass Filter (GLPF) tuned across multiple cutoff frequencies.

## Key Restoration Insights

*   **Metric-Driven Optimization:** The restoration pipeline utilizes the **Structural Similarity Index (SSIM)** as its primary objective function to align recovery with human visual perception rather than pixel-level mathematical variance (PSNR). 
*   **Noise vs. Content:** Empirical testing on identical underlying visual assets (`coins` and `rice` templates) proved that optimal restoration architecture is strictly dictated by the mathematical noise distribution model injected into the environment rather than high-frequency edge textures. Non-linear rank-order filters (**Median**) completely eliminated high-density impulse noise, while continuous variance patterns required localized spatial averaging (**Bilateral** & **Gaussian**).

## Benchmarking Results

| Method / Domain | Dataset Average PSNR | Dataset Average SSIM |
| :--- | :---: | :---: |
| **Spatial Domain (Dynamic Tuning)** | **28.46 dB** | **0.8019** |
| **Frequency Domain (Fixed GLPF)** | 24.10 dB | 0.6273 |

*Spatial domain approaches significantly outperformed global frequency attenuation by preventing the destructive blur of high-frequency edge vectors.*
