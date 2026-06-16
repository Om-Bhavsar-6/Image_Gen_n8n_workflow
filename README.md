# 🤖 Local-to-Cloud AI Image Generator Workflow (n8n + Hugging Face)

A lightweight, automated image generation pipeline built using **n8n** and Hugging Face's modern serverless inference infrastructure. This workflow securely captures a localized text prompt, establishes an authenticated API handshake with the cloud, and returns a high-quality binary image asset.

---

## 🚀 Features

* **Modern Infrastructure:** Fully compatible with Hugging Face's centralized serverless `router` gateway architecture.
* **State-of-the-Art Model:** Utilizes **FLUX.1-schnell** (`black-forest-labs`) for ultra-fast, high-fidelity text-to-image synthesis.
* **Binary Stream Handling:** Bypasses legacy JSON-base64 processing to accept raw `image/png` streams directly into n8n.
* **Easy Customization:** Prompts can be instantly modified inside the localized data fields or hardcoded directly into the API payload.

---

## 🛠️ Prerequisites

Before importing the workflow, make sure you have the following:

1. **n8n** running locally (Desktop App, Docker, or npm instance).
2. A free **Hugging Face Account** ([Sign up here](https://huggingface.co/join)).
3. A Hugging Face **Access Token** with `Read` permissions ([Generate one here](https://huggingface.co/settings/tokens)).

---

## 📦 Installation & Setup

### 1. Clone & Import
1. Download or copy the `workflow.json` file from this repository.
2. Open your local n8n instance canvas.
3. Click anywhere on the blank grid and press **Ctrl + V** (or **Cmd + V** on Mac) to paste and auto-build the layout.

### 2. Configure Your Credentials
1. Double-click the **Hugging Face API** node to open its settings.
2. In the **Headers** section, locate the `Authorization` key.
3. Replace the placeholder text with your real token, ensuring you keep the `Bearer` prefix and space:
```text
   Bearer hf_YOUR_ACTUAL_TOKEN_HERE
