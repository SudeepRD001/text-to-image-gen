# 🎨 Text-to-Image Generator (SDXL Turbo + Gradio)

This project transforms any text prompt into a stunning image using **Stable Diffusion XL Turbo** from Hugging Face. It features a professional, modern **Gradio-based web UI** that supports live preview and **one-click image download**.

---

## ✨ Features

- 🔥 Powered by **Stable Diffusion XL Turbo**
- 💡 Supports any creative text prompt
- 🖼️ Live image preview
- 📥 One-click download in `.png` format
- ⚙️ Built with `diffusers`, `torch`, `gradio`, and `huggingface_hub`

---

## 📸 Sample Output

<img src="assets/output_sample1.png" width="400"/>
<img src="assets/output_sample2.png" width="400"/>

---

## 🛠️ Tech Stack

| Component     | Technology                 |
|---------------|-----------------------------|
| Backend       | PyTorch + Hugging Face Diffusers |
| Frontend UI   | Gradio (Soft theme)         |
| Model         | `stabilityai/sdxl-turbo`    |
| Language      | Python 3.10+                |
| Deployment    | Local via VS Code, optionally deploy to Hugging Face Spaces |

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/SudeepRD001/text-to-image-gen.git
cd text-to-image-gen
```
## 2. Create & Activate Virtual Environment

### Create Virtual Environment
```bash
python -m venv venv
```
### Activate Virtual Environment
```bash
venv\Scripts\activate # Windows
source venv/bin/activate # macOS / Linux
```
## 3. Install Dependencies

> **Prerequisite:** Make sure your (activated) virtual environment is active before running these commands.

```bash
# Install PyTorch with CUDA 12.1 support
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121

# Install the remaining project dependencies
pip install diffusers transformers accelerate safetensors gradio python-dotenv
```

## 4. Set Hugging Face Token

To use models from Hugging Face, you need to authenticate using a **Read** access token.

### 🔐 Steps to Create Hugging Face Access Token

1. Go to [Hugging Face Tokens Page](https://huggingface.co/settings/tokens)
2. **Sign in** or **Sign up** for a free account.
3. Click **“New token”**.
4. Set a name (e.g., `colab-sdxl`).
5. For **Role**, select ✅ **Read** (this is enough for downloading models).
6. Click **Generate**.
7. Copy your new token.

---

### 🧪 Use Your Token in the Code

Replace `"your_huggingface_token_here"` with your actual token:

```python
# Step 1: Login to Hugging Face
from huggingface_hub import login

try:
    login("your_huggingface_token_here")  # Replace this with your actual token
except Exception as e:
    print("❌ Hugging Face login failed:", e)
```
### ⚠️ Do not share your token publicly.
---

## ▶️ Run the App

Once all dependencies are installed and your Hugging Face token is set, you can start the application:

```bash
python texttoimage.py
```
A local Gradio interface will open automatically in your browser, typically at:
http://127.0.0.1:7860
💡 If it doesn’t open automatically, you can manually visit the URL above.

---

## 📜 License

MIT License © 2025 SUDEEP  
Feel free to use, modify, and distribute this project as per the terms of the MIT license.

---

## 🙌 Acknowledgments

- 🤗 [Hugging Face](https://huggingface.co) — for providing model hosting and tools  
- 🌐 [Gradio](https://gradio.app) — for the simple web UI integration  
- 🎨 [Stable Diffusion XL Turbo](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0-turbo) — for the fast, high-quality image generation model

---
