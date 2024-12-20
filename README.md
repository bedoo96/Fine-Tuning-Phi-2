# 🧠 Fine-Tuning Large Language Models (LLMs) with LoRA and Quantization

## Introduction

This project focuses on **fine-tuning a large language model (LLM)** using advanced techniques such as **quantization** and **Low-Rank Adaptation (LoRA)**. The goal is to make the training process more efficient by optimizing memory usage and performance while maintaining high accuracy for tasks like causal text generation.

The project leverages **Hugging Face Transformers**, **LoRA**, and **PyTorch** to fine-tune a pre-trained model on medical data.

---

## Objectives

The primary objectives of the project are:
1. To fine-tune Microsoft's **Phi-2** language model on a medical dataset to enhance its domain-specific accuracy.
2. To optimize training using **4-bit quantization** and **LoRA**, enabling efficient model adaptation with limited resources.
3. To save the fine-tuned model for future use or evaluation on other tasks.

---

## Key Features

1. **4-bit Quantization**: Reduces memory consumption and speeds up training by loading the model in a quantized format.
2. **Low-Rank Adaptation (LoRA)**: A technique that updates specific layers of the model, allowing rapid fine-tuning with minimal computational requirements.
3. **Medical Dataset**: The model is trained on a domain-specific dataset, enhancing its ability to answer medical queries accurately.
4. **Model Saving**: The fine-tuned model is saved for reuse, ensuring it can be deployed or further evaluated in downstream tasks.

---

## Technical Approach

### 1. **Data Preparation**
   - The dataset used is [MedQuad-phi2-1k](https://huggingface.co/datasets/prsdm/MedQuad-phi2-1k), a medical dataset available on Hugging Face.
   - Input prompts are formatted with templates (with and without additional inputs) to standardize the model's input structure.

### 2. **Quantization Configuration**
   - The model is loaded in **4-bit quantized format** using the `BitsAndBytesConfig` library.
   - This configuration significantly reduces memory usage while preserving performance during training.

### 3. **Low-Rank Adaptation (LoRA)**
   - LoRA is used to modify only specific layers of the model, avoiding full parameter updates. This reduces computational load and speeds up training.

### 4. **Training Process**
   - Fine-tuning involves optimized hyperparameters, including learning rates, gradient clipping, and dropout regularization, to ensure effective model adaptation.
   - Training metrics are logged for real-time monitoring.

---

## Technologies Used

- **Python**: Core language for implementing the project.
- **Hugging Face Transformers**: For model loading, training, and evaluation.
  - [Hugging Face Transformers Documentation](https://huggingface.co/transformers/)
- **LoRA (Low-Rank Adaptation)**: For efficient model adaptation.
  - [LoRA Documentation](https://github.com/microsoft/LoRA)
- **PyTorch**: For model training and evaluation.
  - [PyTorch Documentation](https://pytorch.org/)
- **BitsAndBytes**: For memory-efficient model quantization.
  - [BitsAndBytes Documentation](https://github.com/TimDettmers/bitsandbytes)
- **WandB**: For tracking and logging training experiments.
  - [Weights and Biases Documentation](https://wandb.ai/)

---

