# BrainFocus: EEG-Guided ROI Selection for Efficient Vision-Language Models

> **Dataset:** [BrainFocus dataset on IEEE DataPort](https://ieee-dataport.org/documents/brainfocus-dataset-ai-generated-cluttered-scene-images-bounding-boxes-and-vqa-metadata) — **DOI: [10.21227/2vvw-1n73](https://doi.org/10.21227/2vvw-1n73)**. Check the IEEE DataPort record to download the dataset, including generated images, bounding boxes, VQA metadata, and associated documentation.

**Paper:** [BrainFocus: EEG-Guided ROI Selection for Efficient Vision-Language Models](https://arxiv.org/abs/2609.17443), arXiv:2609.17443 (preprint).

## What BrainFocus does

BrainFocus uses an EEG classifier to suggest a visual category (Stage 1), a category-conditioned YOLO detector to locate a candidate region of interest (Stage 2), and a vision-language model to answer a visual question (Stage 3). A crop is sent to Stage 3 only if the Stage 1 confidence passes the EEG gate **and** a matching Stage 2 box exists and passes the ROI gate. Otherwise, use the full image. The fallback keeps unreliable intermediate predictions from forcing a crop.
