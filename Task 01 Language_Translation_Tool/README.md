# Language-Translation-Tool-with-API

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1n2buPVFupMYHrx_teH-KQmvWqT6uQ2ng?usp=sharing)

## Overview

This project is an AI-powered language translation tool capable of translating text between multiple languages. It utilizes transformer-based deep learning models to provide accurate and context-aware translations.

### Key Features:
- **Multi-language Support**: Supports various language pairs.
- **Deep Learning-Based Accuracy**: Uses a state-of-the-art transformer model.
- **Real-time Processing**: Provides fast and efficient translations.
- **User-Friendly Interface**: Built using Gradio for seamless interaction.

### Project Category:
This project falls under **AI for Language Processing**, making language translation accessible and efficient for global communication.

---

## Requirements

### Prerequisites
Ensure you have Python 3.7+ installed and run the following command to install dependencies:

```bash
pip install transformers gradio torch sentencepiece
```

- **`transformers`**: Loads pre-trained language models.
- **`gradio`**: Enables a simple web interface.
- **`torch`**: Provides deep learning support.
- **`sentencepiece`**: Helps tokenize text for translation models.

---

## How It Works

1. **Text Tokenization**: The input is tokenized for processing.
2. **Translation Model Execution**: A transformer-based model generates translations.
3. **Final Output**: The translated text is displayed in the Gradio UI.

---

## Automatic Setup Instructions

1. Click on the **Open in Colab** button.
2. Connect to a Colab runtime.
3. Run all notebook cells sequentially.
4. Use the Gradio interface to translate text.

---

## Manual Setup Instructions

### Step 1: Install Dependencies
Ensure Python 3.7+ is installed and run:

```bash
pip install transformers gradio torch sentencepiece
```

### Step 2: Run the Translation Script

```python
import gradio as gr
from transformers import pipeline

translator = pipeline("translation_en_to_fr")

def translate_text(input_text):
    return translator(input_text)[0]["translation_text"]

interface = gr.Interface(fn=translate_text, inputs="text", outputs="text")
interface.launch()
```

### Step 3: Start the Application
Execute the script, and a Gradio UI will launch in your browser.

---

## Future Enhancements

- **Support for additional languages**
- **Offline translation capabilities**
- **Integration with speech recognition**
- **Enhanced model fine-tuning for specialized translations**

---

## License
This project is licensed under the MIT License.

---


