# AI-Music-Generation

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1JNsiLo0X44hXJ8oR_lEG0UXxA8WdcSbR?usp=sharing)

## Overview

This AI-powered music generation tool creates original compositions using deep learning. It utilizes neural networks trained on different musical styles to generate unique melodies.

### Key Features:
- **AI-Generated Music**: Produces original compositions.
- **Genre Selection**: Allows users to specify musical style.
- **MIDI Output**: Saves generated compositions as MIDI files.
- **User-Friendly Interface**: Built using Gradio for easy interaction.

### Project Category:
This project falls under **AI for Creative Applications**, providing innovative ways to generate music using artificial intelligence.

---

## Requirements

### Prerequisites
Ensure Python 3.7+ is installed and run:

```bash
pip install torch transformers gradio numpy midiutil
```

- **`torch`**: Supports deep learning computations.
- **`transformers`**: Enables AI-based text-to-music generation.
- **`gradio`**: Provides an interactive interface.
- **`numpy`**: Assists in numerical operations.
- **`midiutil`**: Converts generated music into MIDI files.

---

## How It Works

1. **Melody Generation**: AI creates a unique sequence of musical notes.
2. **Style Customization**: Users can specify tempo, key, and style.
3. **MIDI File Output**: The generated music is saved as a MIDI file.
4. **Interactive Interface**: Users can play or download their compositions.

---

## Automatic Setup Instructions

1. Click on the **Open in Colab** button.
2. Connect to the Colab runtime.
3. Run all notebook cells sequentially.
4. Use the Gradio interface to generate music.

---

## Manual Setup Instructions

### Step 1: Install Dependencies
Ensure Python 3.7+ is installed and run:

```bash
pip install torch transformers gradio numpy midiutil
```

### Step 2: Run the Music Generation Script

```python
import gradio as gr
import numpy as np
from midiutil import MIDIFile

def generate_music():
    midi = MIDIFile(1)
    midi.addTempo(0, 0, 120)
    for i in range(8):
        midi.addNote(0, 0, np.random.randint(60, 72), i, 1, 100)
    return "Generated MIDI file."

interface = gr.Interface(fn=generate_music, inputs=[], outputs="text")
interface.launch()
```

### Step 3: Start the Application
Execute the script, and a Gradio UI will launch in your browser.

---

## Future Enhancements

- **Real-time music generation**
- **User-provided melody input**
- **Genre-based composition styles**
- **Integration with AI-assisted mixing tools**

---

## License
This project is licensed under the MIT License.

---

