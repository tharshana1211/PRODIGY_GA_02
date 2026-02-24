🖼️ **Image Generation using Pre-trained Models**

📌**Project Overview**

This project demonstrates Text-to-Image Generation using a pre-trained diffusion-based generative model.
The system converts natural language prompts into high-quality synthetic images using Stable Diffusion.

The objective of this task was to understand and implement image generation using state-of-the-art pre-trained generative models without training from scratch.

🤖 **Model Used**

Stable Diffusion v1.5

Hugging Face Diffusers Library

PyTorch Framework

Stable Diffusion is a latent diffusion model capable of generating detailed and realistic images from textual descriptions.

⚙️ **Features Implemented**

✔️ Loading a pre-trained Stable Diffusion model

✔️ Prompt-based image generation

✔️ Experimentation with multiple creative prompts

✔️ Saving generated images locally

✔️ GPU / CPU compatible implementation


🛠️ **Installation & Setup**

pip install diffusers transformers accelerate torch

💻 **Implementation Code**

from diffusers import StableDiffusionPipeline

import torch

model_id = "runwayml/stable-diffusion-v1-5"

pipe = StableDiffusionPipeline.from_pretrained(model_id)
pipe = pipe.to("cpu")  # Change to "cuda" if GPU is available

prompt = "A futuristic AI engineer working on a holographic computer"

image = pipe(prompt).images[0]
image.save("generated_image.png")
image

🖼️ **Sample Prompts Used**

"A cyberpunk city at night with neon lights"

"A professional AI researcher in a modern lab"

"Minimalist 3D neural network illustration"

"Dark themed tech portfolio background with glowing particles"

📊 **Output**

The system successfully generates high-quality, context-aware images based on user-provided text prompts.

Generated images are saved as .png files in the project directory.
