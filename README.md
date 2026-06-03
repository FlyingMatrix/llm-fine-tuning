# LLM Fine-Tuning

## 🔧 What is LLM Fine-Tuning?

**Fine-tuning a Large Language Model (LLM)** is the process of taking a pre-trained, general-purpose model (like GPT) and training it further on your own dataset so it performs better on a specific task or domain.

- Base model → trained on massive generic data
- Fine-tuned model → adapted for your use case

Example:

- Base LLM: general chatbot
- Fine-tuned LLM: legal assistant, medical summarizer, customer support bot

## 🧠 Why Fine-Tune?

You fine-tune when you want:

- **Better accuracy** in a domain (e.g., finance, healthcare)
- **Consistent tone/style** (e.g., formal, brand voice)
- **Task specialization** (classification, summarization, coding)
- **Reduced prompt engineering effort**

## 🏗️ Types of Fine-Tuning

**1. Full Fine-Tuning**

- Update **all model parameters**
- Requires huge compute (GPUs/TPUs)
- Best performance, but expensive

**2. Parameter-Efficient Fine-Tuning (PEFT)**

Popular methods:

- **LoRA (Low-Rank Adaptation)**
  - Adds small trainable layers
  - Very efficient and widely used
- **Adapters**
  - Insert small modules between layers
- **Prefix / Prompt Tuning**
  - Learn special tokens instead of weights

Most modern applications **use PEFT instead of full fine-tuning**.

## 📉 What LoRA Actually Does?

Instead of updating billions of parameters:

- Original weights stay frozen
- Small trainable matrices are added

Conceptually:

W′=W+ΔW

Where:

- W = original weights
- ΔW = low-rank adaptation

This dramatically reduces:

- VRAM usage
- training cost
- storage size
