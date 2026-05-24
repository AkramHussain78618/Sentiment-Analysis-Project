# 🛒 Amazon Review Sentiment Analyzer

> A beginner-friendly NLP project that uses **pretrained AI models** (VADER & TextBlob) to analyze the sentiment of Amazon customer reviews — built with **Python**, **Flask**, **HTML**, and **CSS**.

## Live Demo
https://sentiment-analysis-project-ezbd.onrender.com/

## 📸 Project Preview

| Section | Description |
|---|---|
| 🏠 Home Page | Hero banner, how-it-works steps |
| 🔬 Analyzer | Paste any review, click Analyze |
| 📊 Results | Emoji, color-coded label, score bars |
| 📌 Samples | Click pre-loaded sample reviews |
| 📋 Dataset | Preview table of Amazon reviews |
| 🧠 Model Info | Explanation of VADER & TextBlob |

---

## 🚀 How to Run This Project

### Step 1: Make sure Python is installed
```bash
python --version
# Should show Python 3.8 or higher
```

### Step 2: (Optional but recommended) Create a virtual environment
```bash
# Create virtual environment
python -m venv venv

# Activate it — on Windows:
venv\Scripts\activate

# Activate it — on Mac/Linux:
source venv/bin/activate
```

### Step 3: Install all required libraries
```bash
pip install -r requirements.txt
```

### Step 4: Download TextBlob's language data (run once)
```bash
python -m textblob.download_corpora
```

### Step 5: Run the Flask app
```bash
python app.py
```

### Step 6: Open your browser
```
http://localhost:5000
```

---

## 📁 Project Folder Structure

```
sentiment_project/
│
├── app.py                    ← Main Flask backend (Python)
├── requirements.txt          ← List of libraries to install
├── README.md                 ← This file
├── Amazon_Reviews.csv        ← Dataset file
│
├── templates/
│   └── index.html            ← Main HTML web page
│
└── static/
    
    │   └── style.css         ← All styling / design
    
        └── main.js           ← Frontend JavaScript logic
```

---

## 🧠 How Sentiment Analysis Works

Sentiment analysis is the process of identifying whether a piece of text expresses a **positive**, **negative**, or **neutral** emotion.

### Two Models Used:

#### 🧪 VADER (Primary)
- **V**alence **A**ware **D**ictionary and s**E**ntiment **R**easoner
- Pretrained on social media, reviews, and short texts
- Returns a **compound score** from -1.0 to +1.0
  - ≥ 0.05 → **Positive**
  - ≤ -0.05 → **Negative**
  - In between → **Neutral**

#### 📝 TextBlob (Secondary)
- Simple NLP library built on NLTK
- Returns **polarity** (-1 to +1) and **subjectivity** (0 to 1)
- Good for comparing with VADER results

### Why Pretrained Models?

| Pretrained Models ✅ | Training Your Own ❌ |
|---|---|
| No data collection needed | Need thousands of labeled examples |
| Ready to use immediately | Takes hours/days to train |
| Built by NLP experts | Risk of poor accuracy |
| Free and open source | Requires GPU / cloud resources |
| Perfect for beginners | Complex to implement |

---

## 📊 Dataset

- **File**: `Amazon_Reviews.csv`
- **Columns used**: `Rating`, `Review Title`, `Review Text`
- **Ratings**: 1 star to 5 stars
- **Source**: Amazon customer reviews

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| **Python 3** | Backend programming language |
| **Flask** | Web framework to serve pages & handle requests |
| **VADER** | Pretrained sentiment analysis model |
| **TextBlob** | Secondary sentiment analysis model |
| **pandas** | Reading and processing the CSV dataset |
| **HTML5** | Web page structure |
| **CSS3** | Styling and responsive design |
| **JavaScript** | Frontend interactivity |
| **Chart.js** | Drawing the bar chart |

---

## ✨ Project Features

- ✅ Analyze any single review in real-time
- ✅ Sentiment result with emoji (😊 / 😞 / 😐)
- ✅ Color-coded result cards (green / red / gray)
- ✅ Visual score bars (Positive / Negative / Neutral %)
- ✅ Dual model comparison (VADER + TextBlob)
- ✅ 6 sample reviews to try instantly
- ✅ Dataset preview table
- ✅ Rating distribution bar chart
- ✅ Fully responsive (works on mobile)
- ✅ Keyboard shortcut: Ctrl+Enter to analyze

---

## 📌 Expected Output

When you type: *"This product is absolutely amazing! Arrived quickly."*

- 😊 **Sentiment: POSITIVE**
- Positive score bar: ~85%
- VADER compound: ~0.85
- TextBlob polarity: ~0.6

When you type: *"Terrible product. Broke after one day. Worst purchase ever."*

- 😞 **Sentiment: NEGATIVE**
- Negative score bar: ~90%
- VADER compound: ~-0.87
- TextBlob polarity: ~-0.7

---

## 👨‍💻 Author

Built as a beginner-friendly internship/portfolio project.  
Perfect for demonstrating NLP, Flask, and web development skills on GitHub.

---

## 📄 License

This project is open source and free to use for learning purposes.
