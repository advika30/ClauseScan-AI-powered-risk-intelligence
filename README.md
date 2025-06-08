# ClauseScan – AI‑Powered Contract Risk Intelligence 📑

A **Streamlit‑based AI tool** that analyzes corporate contracts to classify clauses, assess their legal risk, and generate concise summaries. The project also ships with a **User Management Dashboard** that tracks credentials, flags reused passwords, and monitors login activity.

---

## 🔍 Key Features

### Contract Risk Analyzer

* **Upload contracts** (`.pdf`, `.docx`, `.txt`)
* **Clause detection** – smart NLP‑driven segmentation
* **Clause classification** – Indemnification, Termination, Payment Terms, etc.
* **Risk rating** – High / Medium / Low via BERT‑powered heuristics
* **Automatic summarization** – BART transformer
* **Interactive dashboard** – bar & donut charts; export results to **JSON / CSV**

### User Management Dashboard

* **Secure authentication** – username + hashed password + CAPTCHA
* **Password analysis** – highlights reused credentials
* **Login tracking** – total logins & last‑login timestamp
* **Visual insights** – tabs for reuse frequency, user growth, login activity

---

## 🧠 Tech Stack

* **Frontend**: Streamlit (custom theming)
* **NLP & ML**:

  * BERT – sentence embeddings
  * BART (`facebook/bart-large-cnn`) – summarization
  * spaCy – NER & sentence segmentation
  * Random Forest + TF‑IDF – extractive fallback
* **Libraries**: Transformers, Torch, scikit‑learn, NLTK, pdfminer.six, docx2txt, pandas, plotly, pymongo
* **Database**: MongoDB Atlas

---

## 🚀 Setup

```bash
# 1. Clone
git clone https://github.com/your-username/corporate-clause-risk-analyzer.git
cd corporate-clause-risk-analyzer

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download spaCy model
python -m spacy download en_core_web_sm
```

Create a `.env` file and add your MongoDB URI:

```env
MONGO_URI=mongodb+srv://<user>:<pass>@cluster.mongodb.net
```

Run the app:

```bash
streamlit run bert5.py
```

---

## 🔮 Planned Improvements

* Clause rewriting suggestions for high‑risk clauses
* Clause‑to‑clause contract comparison
* Multilingual support (Spanish, German, …)
* SaaS deployment with admin panel & fine‑grained access control

---

## 📄 License

© 2025 **Advika Gupta** — released under the **MIT License**.
You are free to use, modify, and distribute this work provided proper credit is given and this license notice is retained.
