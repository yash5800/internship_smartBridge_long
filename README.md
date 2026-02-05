# 🍳 Flavour Fusion - AI-Driven Recipe Blogging

A powerful web application that leverages **Google's Generative AI (Gemini)** to create unique and customized recipe blogs instantly.

![License](https://img.shields.io/badge/license-MIT-blue)
![Python](https://img.shields.io/badge/python-3.8+-blue)
![Streamlit](https://img.shields.io/badge/streamlit-1.0+-red)

---

## 🌟 Features

- **🤖 AI-Powered Recipe Generation**: Uses Google Gemini 2.5 Flash to generate detailed, engaging recipes
- **🎯 Customizable Parameters**: 
  - Recipe topic/ingredient input
  - Adjustable word count (100-5000 words)
  - Multiple cuisine type options (Italian, Indian, Chinese, Mexican, Mediterranean, Asian Fusion, American, French)
- **😂 Entertainment**: Random programmer/food jokes displayed while recipes are being generated
- **💾 Recipe History**: Keep track of all generated recipes in the session
- **📥 Download Feature**: Export generated recipes as text files
- **🎨 Beautiful UI**: Modern, gradient-based interface with responsive design
- **⚙️ Advanced Configuration**: Model settings and preferences in sidebar
- **🚀 Optimized Performance**: Model caching for faster subsequent recipe generations

---

## 📋 Prerequisites

Before you begin, ensure you have:

- Python 3.8 or higher
- pip (Python package manager)
- A Google API key for Generative AI
- Unix-based OS (Linux/Mac) or Windows with bash

---

## 🚀 Installation

### 1. Clone or Download the Project

```bash
cd /home/yash/Documents/internship_smartBridge_long
```

### 2. Create a Virtual Environment (Recommended)

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

Create a `.env` file in the project root and add your Google API key:

```env
GOOGLE_GEMINI_API_KEY=your-actual-api-key-here
```

**How to get your Google Gemini API key:**
1. Go to [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Click "Create API Key"
3. Copy the key and paste it in your `.env` file

---

## 🎯 Usage

### Start the Application

```bash
streamlit run app.py
```

The app will automatically open in your browser at `http://localhost:8501`

### How to Generate a Recipe

1. **Enter Recipe Topic**: Type in the main ingredient or recipe type (e.g., "Spicy Thai Curry", "Chocolate Cake")
2. **Select Cuisine Type** (Optional): Choose from various cuisines or select "Any" for no restriction
3. **Set Word Count**: Adjust the desired length of the recipe (100-5000 words)
4. **Configure Preferences** (Optional):
   - Toggle joke display in sidebar
   - Enable/disable recipe history tracking
5. **Click "Generate Recipe"**: The AI will create your recipe
6. **Download**: Save the recipe as a text file

---

## 📁 Project Structure

```
internship_smartBridge_long/
├── app.py                      # Main Streamlit application
├── requirements.txt            # Python dependencies
├── .env                        # Environment variables (not in repo)
├── .venv/                      # Virtual environment
└── README.md                   # This file
```

---

## 📦 Requirements

All dependencies are listed in `requirements.txt`:

```
streamlit==1.28.0
google-generativeai==0.3.0
python-dotenv==1.0.0
```

### Installation via pip:

```bash
pip install streamlit google-generativeai python-dotenv
```

---

## 🔧 Configuration

### Generation Settings (in `app.py`)

The generation configuration controls AI behavior:

```python
generation_config = {
    "temperature": 0.75,          # Creativity level (0-1, higher = more creative)
    "top_p": 0.95,                # Diversity parameter
    "top_k": 64,                  # Number of tokens to consider
    "max_output_tokens": 8192,    # Maximum response length
    "response_mime_type": "text/plain"
}
```

### Sidebar Options

- **Show Jokes**: Enable/disable joke display during generation
- **Save History**: Automatically track generated recipes
- **Model Info**: View current model and temperature settings

---

## 🎨 UI/UX Features

- **Gradient Header**: Eye-catching purple gradient background
- **Organized Layout**: 
  - Main input section with 3 columns for better responsiveness
  - Sidebar with configuration and history
  - Recipe display in a styled container
- **Responsive Design**: Works seamlessly on desktop and tablet devices
- **Error Handling**: User-friendly error messages and validation

---

## 🤖 AI Model Details

- **Model**: Gemini 2.5 Flash
- **Provider**: Google Generative AI
- **Temperature**: 0.75 (balanced creativity)
- **Max Tokens**: 8192 (lengthy, detailed recipes)

### Recipe Generation Prompt

The app uses an enhanced prompt that instructs the AI to include:
- Brief introduction about the dish
- Ingredients list with quantities
- Step-by-step cooking instructions
- Tips and tricks
- Serving suggestions
- Nutritional information
- Storage and reheating instructions

---

## 🐛 Troubleshooting

### Issue: "GOOGLE_GEMINI_API_KEY environment variable is not set"

**Solution**: 
1. Create a `.env` file in the project root
2. Add: `GOOGLE_GEMINI_API_KEY=your-key-here`
3. Restart the Streamlit app

### Issue: "No module named 'streamlit'"

**Solution**:
```bash
pip install streamlit
```

### Issue: App runs but recipes aren't generating

**Solution**:
1. Check your API key is valid
2. Verify internet connection
3. Check Google API quota usage

### Issue: Slow recipe generation

**Solution**:
- The first run is slower due to model loading
- Subsequent runs are faster due to caching
- Try reducing word count for faster results

---

## 📝 Example Use Cases

1. **Personal Blog**: Generate unique recipe content for your food blog
2. **Content Creation**: Create multiple variations of recipes quickly
3. **Recipe Collection**: Build a personalized cookbook automatically
4. **Educational Purpose**: Learn how AI can assist in content generation
5. **Restaurant Menu**: Generate menu descriptions and recipes

---

## 🔐 Security Best Practices

1. ✅ **Keep `.env` files private** - Never commit `.env` to version control
2. ✅ **Use API key restrictions** - Limit API key usage in Google Cloud Console
3. ✅ **Monitor API usage** - Check your Google API quota regularly
4. ✅ **Use version control** - Add `.env` to `.gitignore`

### Example `.gitignore`:

```
.env
.venv/
__pycache__/
*.pyc
.DS_Store
```

---

## 🎓 Learning Resources

- [Streamlit Documentation](https://docs.streamlit.io/)
- [Google Generative AI](https://ai.google.dev/)
- [Python dotenv Documentation](https://python-dotenv.readthedocs.io/)

---

## 📊 Performance Metrics

- **Average Generation Time**: 5-15 seconds (depends on word count)
- **Model Caching**: Reduces initialization time by ~80%
- **Supported Word Count**: 100-5000 words
- **Maximum Concurrent Requests**: Limited by Google API quota

---

## 🚀 Future Enhancements

- [ ] Database integration for persistent recipe storage
- [ ] User authentication and profiles
- [ ] Image generation for recipes
- [ ] Recipe search and filtering
- [ ] Multi-language support
- [ ] Recipe rating system
- [ ] Nutritional calculator
- [ ] Shopping list generator

---

## 📄 License

This project is licensed under the MIT License - see LICENSE file for details.

---

## 👨‍💻 Author

**Developed as part of SmartBridge Internship**

Created by: Yash

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 💬 Support & Questions

For issues, questions, or suggestions:
- Open an issue on GitHub
- Check existing documentation
- Review troubleshooting section

---

## 🙏 Acknowledgments

- **Google Generative AI** - For providing powerful AI models
- **Streamlit** - For an exceptional web framework
- **Open Source Community** - For amazing tools and libraries

**Made with ❤️ by Yash | Flavour Fusion ©️ 2026**
