<!--

This source file is part of the the  Daneshjou Lab projects.

SPDX-FileCopyrightText: 2025 Stanford University and the project authors (see CONTRIBUTORS.md)

SPDX-License-Identifier: MIT

-->

# BiasICL

# In-Context Learning and Demographic Biases of Vision Language Models
This repository contains code and data for the paper ["In-Context Learning and Demographic Biases of Vision Language Models"](https://arxiv.org/html/2503.02334v1).  This work investigates the impact of demographic composition of demonstration prompts on the performance of Vision-Language Models (VLMs) in medical diagnosis using in-context learning (ICL).

## Abstract

Vision language models (VLMs) show promise in medical diagnosis, but their performance across demographic subgroups when using in-context learning (ICL) remains poorly understood. We examine how the demographic composition of demonstration examples affects VLM performance in two medical imaging tasks: skin lesion malignancy prediction and pneumothorax detection from chest radiographs. Our analysis reveals that ICL influences model predictions through multiple mechanisms: (1) ICL allows VLMs to learn subgroup-specific disease base rates from prompts and (2) ICL leads VLMs to make predictions that perform differently across demographic groups, even after controlling for subgroup-specific disease base rates. Our empirical results inform best-practices for prompting current VLMs (specifically examining demographic subgroup performance, and matching base rates of labels to target distribution at a bulk level and within subgroups), while also suggesting next steps for improving our theoretical understanding of these models.

## Project Overview

This project explores the following key questions:

* How does the demographic makeup of the examples provided in the ICL prompt affect the VLM's diagnostic accuracy for different demographic groups?
* Does ICL simply allow the VLM to learn and apply subgroup-specific base rates of disease?
* Are there other, more complex interactions between the prompt demographics and the VLM's predictions?

We investigate these questions using two medical imaging datasets:

### Skin Lesion Malignancy Prediction

The [DDI dataset](https://ddi-dataset.github.io/) is a large dataset of skin images annotated with their Fitzpatrick skin tone along with their corresponding diagnosis. We use this dataset to analyze the performance of VLMs in predicting skin lesion malignancy across different demographic groups.

### Pneumothorax Detection from Chest Radiographs

The [CheXpert dataset](https://stanfordmlgroup.github.io/competitions/chexpert/) is a large dataset of chest radiographs annotated with their corresponding diagnosis. We use this dataset to analyze the performance of VLMs in detecting pneumothorax across different demographic groups.


## Code

The code for this project is organized as follows:

* `data/`: Contains the datasets used in the experiments
* `run*.py`: The experiment scripts for running the experiments with different prompt configurations. 
* `requirements.txt`: List of required Python packages.

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/DaneshjouLab/BiasICL.git

2. **Create a virtual environment (recommended):**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Linux/macOS
   venv\Scripts\activate  # On Windows
   ```

3. **Install the required packages:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the datasets** 

5. **Run the experiments**

## Results

The results of the experiments are stored in `*.pkl` files after the experiments are run, which are ready for preprocessing.

Key findings are summarized in the paper:

[https://arxiv.org/pdf/2503.02334v1](https://arxiv.org/pdf/2503.02334v1)

