# Wllama GGUF Browser Chatbot

This project is a simple web-based chatbot interface for running local LLMs (Large Language Models) in your browser using [wllama](https://github.com/wllama/wllama) and GGUF models from Hugging Face. It demonstrates how to load a quantized Gemma model and interact with it directly in the browser, with no backend server required.

## Features

- Loads a GGUF model (e.g., Gemma 3 1B) from Hugging Face
- Runs entirely in the browser using WebAssembly (WASM)
- Supports streaming responses with live token updates
- Simple, modern chat UI
- No installation or server required (just open the HTML file in a browser)


## How to Use

1. **Download the repository or files** to your computer.

2. **Open `index.html` in a modern browser** (Chrome, Edge, or Firefox recommended).

   > **Note:** The first time you use it, the model (~700MB) will be downloaded from Hugging Face. This may take several minutes depending on your internet speed.

3. **Wait for initialization.** The status bar will show progress as the model loads.

4. **Chat!** Once the model is loaded, type your message and press Enter or click Send.

## Requirements

- Modern browser with WebAssembly and ES modules support
- Sufficient RAM (at least 4GB recommended)
- Internet connection (for model download)

## Model Details

- **Model Repo:** `lmstudio-community/gemma-3-1B-it-qat-GGUF`
- **Model File:** `gemma-3-1B-it-QAT-Q4_0.gguf`
- Model is loaded directly from Hugging Face via the [wllama](https://github.com/wllama/wllama) library

## Troubleshooting

- **Model fails to load or browser crashes:** Make sure you have enough free RAM and are using a 64-bit browser.
- **Multi-threading errors:** If you see errors about `SharedArrayBuffer` or COOP/COEP, try running a local server with proper headers, or use single-threaded mode.
- **Slow performance:** Try closing other tabs or applications to free up memory.

## Credits

- [wllama](https://github.com/wllama/wllama) for the browser LLM runtime
- [Hugging Face](https://huggingface.co/) for model hosting

---

**This project is for demonstration and educational purposes. Running large models in the browser is experimental and may not work on all devices.**
