# The Cultural Ceiling of Large Language Models: Quantifying the Interpretative Friction in Diabetes Stigma Detection

# Abstract

Stigma is not a linguistic pattern but a contextual performance. Generalized LLMs fail because they lack the "cultural vocabulary of specific patient communities.
Current large language models can perform surface-level classification, but they often miss culturally specific meanings in social constructs such as stigma. This study introduces a semi-supervised framework that uses community-specific data to detect these meanings, enabling scalable monitoring of culturally grounded signals in public health.

# Overview

![Technology-animation-gif](https://github.com/HIVE-UofT/Diabetes-Stigma-Detection-Framework/blob/main/Figs/process.png)

## 📁 Repository Structure

```
.
├── Code
│   ├── LLM-data-generation/
│   ├── LLM-fine-tuning/
│   ├── Prompt-Optimization/
│   └── Semi-supervised-learning/
│       └── Ensemble-model-voting/
├── Data
│   ├── Generated-samples/
│   ├── Initial-dataset/
│   ├── Pseudo-labeled-samples/
│   ├── Reddit-datasets/
│   └── Unlabeled-additional-samples/
├── Figs/
├── README.md
```

- **`Code/`** – Contains notebooks and implementations for data generation, prompt optimization, model fine-tuning, and semi-supervised learning workflows.

- **`Code/LLM-data-generation/`** – Scripts for generating stigma-related samples using GPT and Llama models.

- **`Code/LLM-fine-tuning/`** – Notebooks for supervised fine-tuning and evaluation of LLMs.

- **`Code/Prompt-Optimization/`** – DSPy-based pipelines for optimizing prompts across different model families.

- **`Code/Semi-supervised-learning/`** – Implements pseudo-labeling and ensemble strategies to leverage unlabeled data.

- **`Data/Generated-samples/`** – Synthetic datasets produced by LLMs for training and experimentation.

- **`Data/Initial-dataset/`** – Original labeled train/validation/test splits used as the starting point for experiments.

- **`Data/Pseudo-labeled-samples/`** – Automatically labeled samples created via semi-supervised methods and majority voting.

- **`Data/Reddit-datasets/`** – Raw Reddit datasets in `json` format.

- **`Data/Unlabeled-additional-samples/`** – Additional unlabeled data used to expand the training pool.

- **`Figs/`** – Figures and diagrams illustrating the methodology and pipeline.

# Citation
Soon
