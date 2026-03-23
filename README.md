# The Cultural Ceiling of Large Language Models: Quantifying the Interpretative Friction in Diabetes Stigma Detection

## Abstract

This repository contains the code and dataset for the manuscript **The Cultural Ceiling of Large Language Models: Quantifying the Interpretative Friction in Diabetes Stigma Detection** (under review).

This repository contains the implementation of prompt optimization and semi-supervised learning frameworks for reproducing LLM models for contextualized stigma detection in diabetic communities.

## Overview

As the first step, we experimented with commercial (OpenI-GPT4O) and open-source (Llama3.1-8B) LLMs, using various prompt optimization methods to enhance performance for stigma detection. We used our initial human-labeled dataset (available at `/Data/Initial%20dataset` directory).

To further enhance the performance and scalability of the detection models, we developed a semi-supervised learning framework that uses an ensemble of LLMs, guided with a KL-divergence weighting for labeling, for data expansion. The new labeled data samples would be used for supervised fine-tuning (SFT) of Llama3.2-3B, which shows a higher performance compared to prompt-optimized larger models.

![Figure 1.](https://github.com/HIVE-UofT/Diabetes-Stigma-Detection-Framework/blob/main/Figs/process.png)
**Figure 1** illustrates an overview of the study framework in this work. Starting from problem identification by using the collected posts from Type 1 and Type 2 diabetic communities on Reddit, and developing LLM-based models for stigma detection, and evaluating them for the corresponding tasks.

## Repository layout

- **`Code/`** – Contains notebooks and implementations for :

  - **`Code/LLM-fine-tuning/`** – Notebooks for supervised fine-tuning (SFT) and evaluation of Llama3.2-3B.
  - **`Code/Prompt-Optimization/`** – DSPy-based pipelines for optimizing prompts for GPT-4O and LLama3.1-8B.
  - **`Code/Semi-supervised-learning/`** – Implements semi-supervised learning framework.
- **`Data`** - Contains data samples for:
  - **`Data/Initial-dataset/`** – Original human-labeled train/validation/test splits.
  - **`Data/Pseudo-labeled-samples/`** –labeled samples created via semi-supervised methods.
  - **`Data/Reddit-datasets/`** – Raw collected Reddit datasets in `json` format.
  - **`Data/Unlabeled-additional-samples/`** – Unlabeled data used as the input for the semi-supervised learning framework.

- **`Figs/`** – Figures and diagrams illustrating the methodology and pipeline.

## Tutorial

### Prompt optimization
- You can use the corresponding notebooks in `Code/Prompt Optimization`for each model to optimize the model for various prompt optimization methods.
- The dataset for this part is available in `/Data/Initial dataset`.

### Semi-supervised framework
- As the first step, use the notebooks in `/Code/Semi-supervised learning/Ensemble model voting` to generate the initial labels by each LLM in the ensemble group.
- Then use the '/Code/Semi-supervised learning/semi-supervised-ensemble-decision.ipynb' to aggregate the labels by the KL-divergence weighting.
- Finally, use the notebooks in `/Code/LLM fine-tuning` for SFT tuning and evaluation of the LLM.
- The output of this pipeline used in experiments is available in `/Data/Pseudo-labeled samples`.
## Citation
Soon
