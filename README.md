# Customer-Review-Auto-Sorter-NLP-Based-Sentiment-Analysis-Automation
An NLP-based Python automation project that analyzes customer reviews, classifies sentiment as Happy, Neutral, or Angry, categorizes reviews by topics such as Delivery, Price, Quality, and Service, visualizes customer feedback, and automatically identifies urgent negative reviews for real-time monitoring.

# Customer Review Auto-Sorter

### NLP-Based Customer Review Classification and Real-Time Automation

Customer Review Auto-Sorter is a beginner-friendly **Natural Language Processing (NLP) automation project** that automatically analyzes customer reviews, identifies their sentiment, categorizes them by topic, and flags negative reviews for immediate attention.

The project demonstrates how NLP can be combined with **data processing, sentiment analysis, keyword-based classification, visualization, and real-time automation** to help businesses efficiently monitor large volumes of customer feedback.

---

## 🚀 Project Overview

Businesses can receive thousands of customer reviews, making it difficult for support teams to manually analyze every review.

This project provides an automated pipeline that:

- Generates a dataset of **100,000 sample customer reviews**
- Processes large datasets using **chunk-based processing**
- Performs sentiment analysis using **VADER**
- Classifies reviews as **happy, neutral, or angry**
- Categorizes reviews into topics such as:
  - Delivery
  - Price
  - Quality
  - Service
- Generates visual insights using Matplotlib
- Simulates a **real-time review monitoring system**
- Automatically detects negative reviews
- Saves urgent reviews into `urgent_reviews.csv`

---

## 🔄 Project Workflow

```text
Customer Reviews
       │
       ▼
Generate / Load Dataset
       │
       ▼
Chunk-Based Data Processing
       │
       ▼
Sentiment Analysis
       │
       ├── Happy
       ├── Neutral
       └── Angry
       │
       ▼
Topic Classification
       │
       ├── Delivery
       ├── Price
       ├── Quality
       └── Service
       │
       ▼
Visualization & Analysis
       │
       ▼
Real-Time Monitoring
       │
       ▼
Negative Review Detection
       │
       ▼
Urgent Review Alert
       │
       ▼
urgent_reviews.csv
```

---

## 🧠 Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data processing and CSV handling |
| VADER Sentiment | Sentiment analysis |
| Matplotlib | Data visualization |
| Random | Sample review generation |
| Time | Real-time monitoring simulation |
| Jupyter Notebook | Development and experimentation |

---

## 📦 Installation

Install the required Python libraries:

```bash
pip install pandas matplotlib vaderSentiment
```

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/your-username/customer-review-auto-sorter.git
```

### 2. Navigate to the project

```bash
cd customer-review-auto-sorter
```

### 3. Install dependencies

```bash
pip install pandas matplotlib vaderSentiment
```

### 4. Open the notebook

```bash
jupyter notebook review_auto_sorter.ipynb
```

Run the notebook cells sequentially.

---

## 📊 Sentiment Analysis

The project uses **VADER SentimentIntensityAnalyzer** to calculate a compound sentiment score between **-1 and +1**.

The classification logic is:

```text
Score >= 0.3       → Happy
Score <= -0.3      → Angry
Otherwise          → Neutral
```

This allows customer feedback to be automatically separated according to sentiment.

---

## 🏷️ Topic Classification

The project uses keyword-based classification to identify the primary topic of a review.

Current categories include:

```text
Delivery → delivery, shipping
Price    → price, cost
Quality  → quality, build
Service  → service
Other    → no matching keyword
```

The topic and sentiment information can then be combined to understand where customers are experiencing problems.

---

## 📈 Data Visualization

The notebook creates a cross-tabulation of:

```text
Topic × Sentiment
```

and generates a bar chart showing the number of reviews categorized by topic and sentiment.

This can help identify areas where customers are particularly dissatisfied.

---

## ⚡ Real-Time Automation

The project also includes a simulated real-time monitoring system.

New reviews are periodically generated and automatically processed:

```text
New Review
    ↓
Sentiment Detection
    ↓
Topic Detection
    ↓
Is sentiment Angry?
    ↓
   YES
    ↓
Generate ALARM
    ↓
Save to urgent_reviews.csv
```

Currently, the notebook simulates a live feed using generated reviews. In a production environment, the same architecture could be connected to an API, database, message queue, or external review platform.

---

## 📁 Output Files

### `reviews.csv`

Contains the generated dataset of **100,000 customer reviews**.

Expected structure:

```text
review
----------------------------
Shipping was excellent
The price is terrible
Customer service was great
...
```

### `urgent_reviews.csv`

Contains reviews identified as **angry/negative**, along with their detected topic.

Example structure:

```text
review                         topic
------------------------------------------------
Shipping was horrible         delivery
The price is terrible         price
Service team was awful        service
```

---

## 🔧 Customization

The notebook can be extended for real-world applications.

### Use Real Customer Reviews

Replace the generated dataset with your own CSV file containing a:

```text
review
```

column.

### Add More Topics

Modify the keyword dictionary:

```python
keywords = {
    "delivery": ["delivery", "shipping"],
    "price": ["price", "cost"],
    "quality": ["quality", "build"],
    "service": ["service"],
}
```

### Connect a Real-Time Data Source

The `new_reviews()` function can be replaced with a real API, database, or file-monitoring mechanism.

### Add Email or Slack Alerts

The current alarm:

```python
print("ALARM...")
```

can be replaced with an email, Slack webhook, or other notification mechanism.

### Use Advanced NLP Models

For more complex language understanding, VADER can be replaced with a transformer-based sentiment model.

Possible future models include:

```text
BERT
RoBERTa
DistilBERT
Transformers-based sentiment models
```

---

## 🎯 Learning Objectives

This project demonstrates practical applications of:

- Natural Language Processing
- Sentiment Analysis
- Text Classification
- Keyword-Based Categorization
- Large Dataset Processing
- Data Visualization
- Real-Time Automation
- Python Data Engineering
- Customer Feedback Analytics

---

## 🌍 Real-World Applications

The same approach can be adapted for:

- E-commerce review monitoring
- Customer support automation
- Product feedback analysis
- Complaint detection
- Social media monitoring
- Service quality monitoring
- Customer experience analytics
- Automated support ticket prioritization

---

## 🔮 Future Enhancements

Potential improvements include:

- Replace keyword classification with machine-learning classification
- Use Transformer-based NLP models
- Support multilingual reviews
- Detect sarcasm and contextual sentiment
- Connect directly to live review APIs
- Add email/Slack notifications
- Build a Streamlit dashboard
- Store results in a database
- Add sentiment trends over time
- Deploy the pipeline as a web API

---

## 👨‍💻 Project Structure

```text
customer-review-auto-sorter/
│
├── review_auto_sorter.ipynb
├── reviews.csv
├── urgent_reviews.csv
├── README.md
└── requirements.txt
```

---

## 📜 License

This project is intended for **educational, demonstration, and research purposes**. You may modify and extend the implementation for your own projects.

---

## ⭐ Project Highlights

> **100,000 Reviews → NLP Sentiment Analysis → Topic Classification → Visualization → Real-Time Negative Review Detection → Automated Alerts**

This project demonstrates how a simple NLP pipeline can be transformed into a practical **customer feedback automation system**.
