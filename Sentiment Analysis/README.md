# Advanced Sentiment Analysis 🧠✨

A robust and intelligent AI-powered sentiment analysis web application with multilingual support, emotion recognition, batch processing, and translation features. Built using Flask and modern NLP tools.

---

## 📌 Table of Contents

- [Features](#features)
- [Quick Start](#-quick-start)
- [Dependencies](#-dependencies)
- [Usage](#-usage)
- [API Endpoints](#api-endpoints)
- [Project Structure](#️-project-structure)
- [Configuration](#-configuration)
- [Supported Languages](#-supported-languages)
- [Technical Features](#-technical-features)
- [Analysis Methods](#-analysis-methods)
- [Limitations](#-limitations)
- [Contributing](#-contributing)
- [License](#-license)
- [Acknowledgments](#-acknowledgments)
- [Support](#-support)
- [Future Enhancements](#-future-enhancements)

---

## 🧩 Features

### 🔍 Core
- Real-time sentiment and emotion analysis
- 12+ language support
- Unified English-based analysis for consistency
- Confidence scores and emotion detection (based on Plutchik's model)

### 📁 Analysis Modes
- Single text
- Batch processing (manual input or `.txt` file upload)
- Cross-language sentiment comparison

### ⚙️ Advanced
- Automatic language detection
- Translation (optional, toggleable)
- Progress bars, emoji indicators, detailed VADER scores

---

## 🚀 Quick Start

### Prerequisites

- Python 3.7+
- pip

### Installation

```bash
git clone https://github.com/yourusername/advanced-sentiment-analysis.git
cd advanced-sentiment-analysis
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
python sentiment.py
```

Open in browser: `http://localhost:5000`

---

## 📦 Dependencies

```
Flask>=2.0.0
nltk>=3.8
textblob>=0.17.1
langdetect>=1.0.9
deep-translator>=1.11.4
Werkzeug>=2.0.0
```

---

## 🎯 Usage

### Web Interface
- Navigate to `http://localhost:5000`
- Use “Single Text”, “Batch Analysis”, or “Compare Languages” tabs
- View results with visual breakdown, scores, language, and emotion

---

## 📡 API Endpoints

### Analyze Single Text
```http
POST /analyze
Content-Type: application/json

{
  "text": "I love this project!"
}
```

### Batch Analysis
```http
POST /analyze-batch
Content-Type: application/json

{
  "texts": ["Happy text", "Sad one", "Neutral mood"]
}
```

### Compare Languages
```http
POST /compare-analysis
Content-Type: application/json

{
  "texts": ["I love this!", "¡Me encanta esto!", "J'adore ça!"]
}
```

---

## 🏗️ Project Structure

```
advanced-sentiment-analysis/
├── sentiment.py              # Main Flask app
├── index.html                # HTML frontend
├── requirements.txt          # Python packages
├── static/                   # CSS/images (optional)
├── temp_uploads/             # For uploaded .txt files
└── README-DEV.md             # Developer documentation
```

---

## 🔧 Configuration

### Environment Variables

| Variable           | Description                                 | Default     |
|--------------------|---------------------------------------------|-------------|
| `FLASK_ENV`        | Flask mode                                  | development |
| `MAX_CONTENT_LENGTH` | Max file upload size                       | 16MB        |
| `TRANSLATION_ENABLED` | Toggle translation                       | True        |

---

## 🌍 Supported Languages

| Language   | Code | Native Name   |
|------------|------|----------------|
| English    | en   | English        |
| Spanish    | es   | Español        |
| French     | fr   | Français       |
| German     | de   | Deutsch        |
| Italian    | it   | Italiano       |
| Portuguese | pt   | Português      |
| Russian    | ru   | Русский        |
| Japanese   | ja   | 日本語          |
| Korean     | ko   | 한국어          |
| Chinese    | zh   | 中文            |
| Arabic     | ar   | العربية         |
| Hindi      | hi   | हिन्दी          |

---

## 🎨 Technical Features

### Frontend
- Responsive UI with animations and visual feedback
- File drag & drop support
- Emotion emojis and progress indicators

### Backend
- Flask server with modular route handling
- Error handling, validation, and safe file handling
- Optional translation with Deep Translator
- NLTK + TextBlob + VADER for NLP processing

---

## 📊 Analysis Methods

### Sentiment Detection
- VADER for polarity scores (compound, pos, neu, neg)
- Classification thresholds:
  - Positive ≥ 0.05
  - Negative ≤ -0.05
  - Neutral: in-between

### Emotion Detection
- Keyword-based and context-driven
- Based on 8 emotions:
  - Joy, Sadness, Anger, Fear, Disgust, Surprise, Trust, Anticipation

### Translation
- Integrated via `deep-translator`
- Used to normalize text to English before analysis (optional)

---

## 🚨 Limitations

- Max 50 texts per batch
- Max file size: 16MB
- Internet required for translation
- Keyword-based emotion recognition may have edge-case inaccuracies

---

## 🔮 Future Enhancements

- [ ] Real-time updates
- [ ] Auth system (user login, API key)
- [ ] Export analysis (CSV/JSON)
- [ ] PostgreSQL or MongoDB integration
- [ ] Data visualizations (charts, graphs)
- [ ] Model training on custom datasets

---
