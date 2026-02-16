# 🍳 Flavour Fusion - AI Recipe Blogging

Generate unique, customized recipes using **Google's Gemini AI**.

## Features

- 🤖 AI-powered recipe generation
- 🎨 Beautiful, responsive UI
- 📥 Download recipes as text files
- 💾 Recipe history tracking
- 🎯 Customizable word count (100-5000 words)
- 8 cuisine types to choose from

## Quick Start

### Installation

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

### Setup

Create `.env` file with your Google API key:
```
GOOGLE_GEMINI_API_KEY=your-key-here
```

Get your key from [Google AI Studio](https://aistudio.google.com/app/apikey)

### Run

```bash
streamlit run app.py
```

Open `http://localhost:8501` in your browser.

## Usage

1. Enter a recipe topic (e.g., "Spicy Thai Curry")
2. Choose a cuisine type or select "Any"
3. Set desired word count
4. Click "Generate Recipe"
5. Download the generated recipe

## Requirements

- `streamlit` - Web framework
- `google-generativeai` - Google Gemini API
- `python-dotenv` - Environment variable management

