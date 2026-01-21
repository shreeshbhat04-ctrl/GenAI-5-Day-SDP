# SDP Notebooks Guide

## Overview
This folder contains Jupyter notebooks for exploring Large Language Models (LLMs) and image generation using AI.

---

## 📓 SDP_day_1.ipynb
**Topic:** Text Generation with Mistral-7B LLM

### What it does:
- Installs required libraries: `transformers`, `accelerate`, `torch`
- Loads the **Mistral-7B-Instruct-v0.2** model
- Creates a text generation pipeline
- Generates responses based on prompts about LLM capabilities

### Key cells:
1. **Installation** - Sets up dependencies
2. **Model Loading** - Loads Mistral-7B from Hugging Face
3. **Prompt Generation** - Takes user prompts and generates text responses

### Usage:
Run all cells sequentially. The model will generate text based on the provided prompt.

---

## 📓 Day2.ipynb
**Topic:** Text Generation & Image Generation (Stable Diffusion)

### Part 1: Text Generation (distilGPT2)
- Loads a lightweight text generation model
- Demonstrates few-shot prompting for sentiment classification
- Shows how to generate text completions

### Part 2: Image Generation (Stable Diffusion v1.5)
- Installs **diffusers** library for image generation
- Loads the Stable Diffusion model
- Generates images from text prompts
- Features:
  - Customizable inference steps (10-50)
  - Adjustable guidance scale (1-15)
  - Saves generated images locally

### Key cells:
1. **Dependencies** - Installs transformers, torch, diffusers, accelerate
2. **Text Generation** - Few-shot prompting example
3. **Image Generation** - Loads Stable Diffusion and generates images
4. **Utilities** - Helper function for generating images

### Usage:
- Run cells sequentially up to the `generate_image()` function
- Use the function with custom prompts to generate images
- Images are saved as PNG files

---

## 🚀 Requirements
```
transformers
torch
accelerate
diffusers
huggingface_hub
```

## 🎮 Interactive Features (Local Use Only)
The original Day2.ipynb includes a Gradio web UI that allows interactive image generation with sliders for:
- Prompt input
- Inference steps
- Guidance scale

This UI is available when running locally but cannot be displayed on GitHub. To use the interactive interface, run the notebook in Jupyter/Colab and uncomment the Gradio cells.

---

## 📝 Notes
- Models require GPU for optimal performance (CUDA recommended)
- First model load may take time (minutes) as models are downloaded
- Image generation produces `generated_image.png` files
- Both notebooks use Hugging Face models and require internet connection for initial model download

