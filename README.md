# DTMF Generator

A simple Jupyter Notebook file that generates and plays [**DTMF (Dual-Tone Multi-Frequency)**](https://grokipedia.com/page/Telephone_keypad#audio-signaling) tones - the sounds produced when dialing numbers on a telephone keypad.

This project was originally written many years ago, but I decided to open-source it as I have no real use for this, and it's pretty much complete as-is.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/dmx3377/dtmf-gen/blob/main/dtmf_gen.ipynb)


---

## What it does
- Generates DTMF tones using the standard frequency pairs
- Supports digits `0–9`, `*`, and `#`
- Plays the generated audio directly in the notebook

---

## How it works
Each digit is represented by **two sine waves**:
- One low-frequency tone
- One high-frequency tone

These tones are summed and played sequentially with short pauses between digits.

---

## Requirements
- Python 3
- numpy
- Jupyter Notebook *(or Google Colab)*

***Install locally:***
`pip install numpy`


# Usage

1. Open the notebook
2. Edit the number:
`DIAL_NUMBER = "01234567890"`
3. Run all cells
4. The sound will output the inputted number in `DIAL_NUMBER` as a DTMF tone.

## Parameters
You can adjust:

* Sampling rate
* Tone duration
* Pause duration between tones

**Example:**
```python
SAMPLING_RATE = 48000
SIGNAL_DURATION = 0.075
PAUSE_DURATION = 0.05
```
---

# License
This software is licensed under [the Unlicense.](LICENSE)
