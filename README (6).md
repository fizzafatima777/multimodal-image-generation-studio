# 🎨 Multimodal Image Generation Studio

A lightweight, notebook-based AI image generation tool that converts text prompts into high-quality digital artwork — complete with aspect-ratio presets, automatic retry logic, image integrity verification, style modifiers, and an interactive widget-based UI.

Built during my internship at **Decode Labs**.

---

## 📌 Overview

**Multimodal Image Generation Studio** is a Google Colab / Jupyter notebook project that turns natural-language text descriptions into AI-generated images using the [Pollinations.ai](https://pollinations.ai/) image generation API. It goes beyond a simple "prompt → image" script by adding production-style reliability features: retry handling for failed requests, image integrity checks, ready-made aspect ratio presets, and a set of curated art style modifiers — all wrapped in a simple interactive UI built with `ipywidgets`.

## ✨ Features

- **Text-to-Image Generation** — Generate digital artwork directly from a text prompt.
- **Aspect Ratio Presets** — Choose from Square (1:1), Landscape (16:9), or Portrait (9:16) presets suited for social media, banners, or wallpapers.
- **Automatic Retry Logic** — Failed or timed-out requests are automatically retried with randomized backoff (jitter) for reliability.
- **Image Integrity Verification** — Downloaded images are validated to ensure they aren't corrupted or incomplete before being displayed.
- **Style Modifiers** — Apply predefined art styles (Cyberpunk, Minimalism, Watercolor, Cinematic, Anime) on top of any prompt.
- **Interactive Widget UI** — A simple, no-code interface built with `ipywidgets` for entering prompts and selecting options directly inside the notebook.

## 🛠️ Tech Stack

- **Python 3**
- [`requests`](https://pypi.org/project/requests/) — for HTTP requests to the image generation API
- [`Pillow (PIL)`](https://pypi.org/project/Pillow/) — for image validation/integrity checks
- [`ipywidgets`](https://pypi.org/project/ipywidgets/) — for the interactive UI
- **Pollinations.ai API** — free text-to-image generation backend
- **Jupyter Notebook / Google Colab**

## 📂 Project Structure

```
Multimodal-Image-Generation-Studio/
│
├── Multimodal_Image_Generation_Studio.ipynb   # Main notebook
└── README.md                                  # Project documentation
```

## 🚀 Getting Started

### Prerequisites

Make sure you have Python 3.8+ installed, then install the required packages:

```bash
pip install requests pillow ipywidgets
```

### Running the Notebook

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/Multimodal-Image-Generation-Studio.git
   cd Multimodal-Image-Generation-Studio
   ```
2. Open the notebook in Jupyter or upload it to [Google Colab](https://colab.research.google.com/).
3. Run all cells in order.
4. Use the interactive widgets at the bottom of the notebook — enter a prompt, pick an aspect ratio, and generate your image.

### Example Usage

```python
generate_image_pro("a red apple on a table", "Square (1:1)")
```

This generates a 1024x1024 image based on the given prompt, with retries and integrity checks handled automatically.

## 🎨 Available Style Modifiers

| Style       | Effect                                              |
|-------------|------------------------------------------------------|
| Cyberpunk   | Neon lights, futuristic, high contrast               |
| Minimalism  | Clean lines, simple, negative space                  |
| Watercolor  | Soft edges, artistic, painted look                   |
| Cinematic   | Dramatic lighting, movie-still aesthetic, 8k detail  |
| Anime       | Vibrant colors, detailed illustration style          |

## 🔮 Future Improvements

- Add support for negative prompts
- Batch image generation
- Local image gallery / history viewer
- Deploy as a standalone web app (Streamlit/Gradio)

## 🙋‍♂️ Author

Developed as part of an internship project at **Decode Labs**.

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
