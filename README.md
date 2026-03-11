# Obstetric Violence Detection on Twitter

This repository contains the resources associated with the study of **obstetric violence (OV) narratives on Twitter**. The project focuses on identifying and classifying tweets that discuss or report experiences of obstetric violence, a form of gender-based violence that occurs during pregnancy, childbirth, and postpartum medical care.

The repository accompanies the research work analyzing the use of **large language models (LLMs)** and classical machine learning approaches to classify tweets related to obstetric violence.

## Project Overview

The main goals of this project are:

- To build a **manually annotated corpus of tweets** related to obstetric violence.
- To categorize tweets according to:
  - **Narrative type** (e.g., activism, testimonies, or other forms of discourse)
  - **Presence of obstetric violence (OV)**
- To evaluate the performance of different approaches for tweet classification, including:
  - **Zero-shot classification using large language models (LLMs)**
  - **Classical supervised baselines such as Bag-of-Words + SVM**

The dataset used in this study consists of **2,157 tweets**, which were manually annotated following a detailed annotation guideline.

## Dataset

The dataset contains tweets related to obstetric violence collected from Twitter using relevant keywords.

Each tweet was manually annotated with the following labels:

### Narrative category
- Activism to highlight obstetric violence
- Obstetric violence narrative
- Non obstetric violence

### Type of obstetric violence (multi-label)
- Physical violence
- Psychological violence
- Institutional violence
- Other categories defined in the annotation guide

The dataset is **highly imbalanced**, as only a small portion of tweets contain explicit obstetric violence narratives.

## LLM Evaluation

The following large language models were evaluated using **zero-shot classification**:

- ChatGPT
- Copilot
- Meta AI

### Important Reproducibility Note

All prompts used to query the LLMs were executed **manually through the official web interfaces of each model**, rather than through APIs or automated scripts.

Specifically:

- ChatGPT responses were obtained via the ChatGPT web interface
- Copilot responses were obtained via the Microsoft Copilot web interface
- Meta responses were obtained via the Meta AI web interface

This approach was adopted to reflect **typical real-world usage scenarios** and ensure comparability across systems.

The exact prompts used in the experiments are documented in the **`prompts`** file.

## Baseline Models

In addition to the LLM-based experiments, we implemented a classical supervised baseline:

**Bag-of-Words (TF-IDF) + Support Vector Machine (SVM)**

This baseline provides a reference point for comparing the performance of zero-shot LLM approaches with traditional machine learning methods for short-text classification.

## Evaluation Metrics

Models were evaluated using the following metrics:

- Precision
- Recall
- F1-score
- Macro-average F1-score
- Accuracy

## Ethical Considerations

This research addresses a sensitive topic related to gender-based violence. All data used in this project comes from **publicly available tweets**, and the dataset is intended solely for **research purposes** related to social media analysis and violence detection.

Researchers using this dataset should carefully consider the ethical implications when analyzing narratives related to personal experiences of violence.

## Citation

If you use this dataset or repository in your research, please cite the corresponding paper.

```bibtex
@article{vazquez2026ovtweets,
  title   = {Detecting Obstetric Violence Tweets from Mexico: Annotation Guidelines and Classification with LLMs},
  author  = {Mónica Vázquez-Hernández, Helena Gómez-Adorno, Natalia Lerín-Hernández,
     Israel Islas Barajas, Orlando Ramos-Flores},
  journal = {IEEE Latin American Transactions},
  year    = {2026}
}
```
