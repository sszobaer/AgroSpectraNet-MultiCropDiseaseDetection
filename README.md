# AgroSpectraNet

**AgroSpectraNet** is a deep learning-based framework for multi-crop disease detection. It is designed to accurately classify diseases across multiple crops under real-world conditions, leveraging both local and global image features to ensure robust performance. This project aims to provide a practical tool for precision agriculture and early disease detection, facilitating healthier crop management and improved yields.

---

## Table of Contents

* [Overview](#overview)
* [Features](#features)
* [Dataset](#dataset)
* [Methodology](#methodology)
* [Installation](#installation)
* [Usage](#usage)
* [Results](#results)
* [Limitations & Future Work](#limitations--future-work)

---

## Overview

AgroSpectraNet addresses the challenges faced in automated crop disease detection by integrating:

* A lightweight **EfficientNet-B0 backbone** for local region-of-interest (ROI) extraction.
* **ConvNeXt-Tiny** architecture for capturing global context.
* Real-time deployment capabilities suitable for mobile or edge devices.

The framework has been trained on a diverse dataset of images representing multiple crops and disease types, ensuring robustness against variations in environmental conditions, lighting, and background noise.

---

## Features

* Multi-crop disease detection.
* Combines local and global image features for improved accuracy.
* Lightweight and efficient, suitable for real-time deployment.
* Data preprocessing, augmentation, and normalization integrated.
* Modular design for easy extension to additional crops or diseases.

---

## Dataset

* Collected a total of **18,592 images** across **six crop types**.
* Includes both healthy and diseased samples.
* Data preprocessing steps included:

  * Removal of duplicates and corrupted images
  * Standardization of image dimensions
  * Data augmentation (rotation, flipping, brightness adjustment)

---

## Methodology

1. **Data Preprocessing & Augmentation:** Ensures high-quality input data for model training.
2. **Model Architecture:**

   * EfficientNet-B0 for local ROI extraction.
   * ConvNeXt-Tiny for global context representation.
3. **Training:**

   * Optimized using Adam optimizer with a suitable learning rate scheduler.
   * Binary cross-entropy or categorical cross-entropy as the loss function.
4. **Evaluation:**

   * Metrics include accuracy, precision, recall, F1-score, and confusion matrix visualization.
   * Cross-validation to ensure generalization.

---

## Installation

1. Clone this repository:

```bash
git clone https://github.com/your-username/AgroSpectraNet.git
```

2. Navigate to the project directory:

```bash
cd AgroSpectraNet
```

3. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
```

4. Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Usage

1. Place your dataset in the `data/` directory.
2. Update configuration in `config.py` (paths, hyperparameters).
3. Train the model:

```bash
python train.py
```

4. Evaluate the model:

```bash
python evaluate.py
```

5. Generate predictions on new images:

```bash
python predict.py --image_path path/to/image.jpg
```

---

## Results

* Achieved **high accuracy across multiple crop types**.
* Confusion matrix and performance metrics can be found in the `results/` directory.
* The trained model is optimized for **real-time inference** on edge devices.

---

## Limitations & Future Work

* Current model trained on six crops; future work could extend this to additional crops.
* Model performance may degrade under extreme environmental conditions.
* Integration with a mobile app or edge deployment platform is planned.

---

