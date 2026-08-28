# AI Virtual Try-On Generator (n8n)

This workflow transforms simple product images and a character photo into **high-quality advertisement images** using AI. It uses the `google/gemini-2.5-flash-image` model via **OpenRouter** to generate a photorealistic fashion model wearing your product.

## ✨ Features
- Upload a **product image** (PNG/JPG) and a **character image**.
- Select a **style** (Natural, Urban, Studio, etc.).
- Automatically generates an advertisement image.
- (Optional: Add Replicate API to generate a 360° video).

## 📁 Project Structure
- `workflow.json` – The n8n workflow file.
- `workflow.png` – A visual diagram of the workflow.
- `README.md` – This file.

## 🛠️ How to Use
1. Import `workflow.json` into your n8n instance.
2. Create an **OpenRouter** account and get an API key.
3. Configure the OpenRouter credential in n8n.
4. Activate the workflow and fill out the form.

## 🏗️ Workflow Phases
1. **Input & Image Prep:** Converts uploaded files to Base64.
2. **Image Generation:** Calls OpenRouter with the character + product images.
3. **Image Processing:** Extracts and converts the generated image to a downloadable file.
4. **Output:** Displays the result to the user.

## 🧰 Built With
- [n8n](https://n8n.io/)
- [OpenRouter](https://openrouter.ai/)
- [Gemini 2.5 Flash Image](https://openrouter.ai/google/gemini-2.5-flash-image)

## ⚠️ Notes
This is a simple advertisement image generator. To add video generation, integrate Replicate's SV3D model.
