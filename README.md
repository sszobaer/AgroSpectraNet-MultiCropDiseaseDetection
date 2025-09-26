# AgroSpectraNet

**AgroSpectraNet** is a deep learning framework for multi-crop disease detection, designed to accurately classify diseases across multiple crops under real-world conditions. By leveraging both local and global image features, it provides robust performance, making it a practical tool for precision agriculture and early disease detection.

---

## Table of Contents

* [Overview](#overview)
* [Authors](#authors)
* [Features](#features)
* [Dataset](#dataset)
* [Methodology](#methodology)
* [Installation](#installation)
* [Usage in JupyterLab](#usage-in-jupyterlab)
* [Results](#results)
* [Limitations & Future Work](#limitations--future-work)

---

## Overview

AgroSpectraNet addresses challenges in automated crop disease detection by integrating:

* A lightweight **EfficientNet-B0 backbone** for local region-of-interest (ROI) extraction.
* **ConvNeXt-Tiny** architecture for capturing global context.
* Real-time deployment capabilities suitable for mobile or edge devices.

The framework has been trained on a diverse dataset of images representing multiple crops and disease types, ensuring robustness against variations in lighting, background, and environmental conditions.

---
## Authors

| Author                 | Contribution                                                                                                   |
| ---------------------- | -------------------------------------------------------------------------------------------------------------- |
| **S. S. Zobaer Ahmed** | Conducted the main experiments, wrote the Methodology and Results Analysis sections, reviewed selected papers. |
| **Barno Biswas**       | Wrote the Conclusion section, assisted with experiments, helped merge the dataset, reviewed papers.            |
| **Tanisha Fairooz**    | Wrote the Introduction section, collected dataset, reviewed additional papers for Introduction.                |
| **Samsun Nahar Eity**  | Collected dataset, wrote the Data Collection section with 6 pie charts, reviewed papers.                       |

---
## Features

* Multi-crop disease detection.
* Combines local and global image features for improved accuracy.
* Lightweight and efficient, suitable for real-time deployment.
* Data preprocessing, augmentation, and normalization included.
* Interactive exploration and visualization through Jupyter notebooks.

---

## Dataset

* Contains **18,592 images** across **six crop types**.
* Includes both healthy and diseased samples.
* Preprocessing steps applied:

  * Removal of duplicates and corrupted images
  * Standardization of image dimensions
  * Data augmentation (rotation, flipping, brightness adjustment)

---

## Methodology

1. **Data Preprocessing & Augmentation:** Ensures high-quality input for training.
2. **Model Architecture:**

   * EfficientNet-B0 for local ROI extraction
   * ConvNeXt-Tiny for global context
3. **Training:**

   * Optimized using Adam with learning rate scheduling
   * Binary or categorical cross-entropy loss
4. **Evaluation:**

   * Metrics: accuracy, precision, recall, F1-score
   * Confusion matrix visualization within notebooks
   * Cross-validation for generalization

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/AgroSpectraNet.git
cd AgroSpectraNet
```

2. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Launch JupyterLab:

```bash
jupyter lab
```

---

## Usage in JupyterLab

1. Open the notebooks in the `notebooks/` directory.
2. Configure dataset paths and hyperparameters in `config.py` if required.
3. Execute cells interactively to:

   * Preprocess and augment data
   * Train the model
   * Evaluate performance metrics
   * Generate predictions on new images
4. Visualize results such as accuracy curves, confusion matrices, and ROC curves directly in the notebook.

---

## Results

* High classification accuracy across multiple crops.
* Interactive plots and confusion matrices generated in notebooks.
* Model optimized for real-time inference on edge devices.

---

## Limitations & Future Work

* Currently trained on six crops; future extensions can include more crops.
* Model performance may degrade under extreme environmental conditions.
* Plans to integrate with a mobile or edge deployment platform for in-field usage.
Here’s a **formal IEEE-style Acknowledgements section** suitable for a paper or thesis for your AgroSpectraNet project:

---

## Acknowledgements

The authors would like to express their sincere gratitude to the following:

* The developers of **PyTorch** and **Torchvision** for their open-source frameworks and pretrained models, which were instrumental in conducting the experiments.
* 🎓 **Jubayer Ahamed**, Lecturer, Department of Computer Science, AIUB, for his continuous guidance, constructive feedback, and encouragement throughout the development and execution of this project.

Their contributions have greatly assisted in the successful completion of this research.

