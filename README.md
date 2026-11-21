
# Continuous LoRA Fine-Tuning Pipeline

## Project Overview

This project implements a continuous fine-tuning pipeline for a Large Language Model (LLM) specialized in Customer Support.

The objective is to continuously improve the model using new instruction datasets while ensuring that general capabilities do not regress.

## Base Model

- Model: Qwen2.5-1.5B-Instruct
- Fine-tuning: QLoRA
- Quantization: 4-bit
- Domain: Customer Support

## Pipeline Architecture

1. Data Ingestion
2. Data Processing
3. Tokenization & Data Versioning
4. QLoRA Fine-Tuning
5. Model Evaluation
6. Quality Gate
7. Model Registry & Versioning
8. Deployment

## Continuous Training Strategy

Two successive training cycles:

- Cycle 1: First training dataset (400 examples)
- Cycle 2: New training dataset (200 examples)

Validation dataset: 100 examples.

Test dataset: 100 examples.

## Evaluation Metrics

- Exact Match
- BERTScore
- LLM-as-Judge
- General Capability Regression

## MLOps Tools

- Git & GitHub
- Google Colab
- DVC
- MLflow
- Python
- Hugging Face
- GitHub Actions

## Project Structure

- `data/`: datasets
- `notebooks/`: Google Colab notebooks
- `src/`: reusable Python modules
- `configs/`: training configurations
- `reports/`: evaluation reports
- `models/`: model metadata and adapter references
- `tests/`: automated tests

## Dataset

Source: [Bitext Customer Support Dataset](https://huggingface.co/datasets/bitext/Bitext-customer-support-llm-chatbot-training-dataset)

The dataset is synthetic and in English.

## Execution Environment

Development: Windows + VS Code.

GPU training: Google Colab.

## Project Status

Currently implementing the data preparation and versioning stages.
