ClauseScan - AI powered contract risk analyzer 📑
A Streamlit-based AI-powered tool that analyzes corporate contracts to classify clauses, assess legal risk levels, and provide summaries.
Includes a built-in User Management Dashboard to monitor user credentials, detect reused passwords, and track login activity.

🔍 Key Features
🔹 Contract Risk Analyzer
📄 Upload Contracts: Supports .pdf, .docx, and .txt formats.

🧠 Clause Detection: Smart splitting of contracts into logical clauses using NLP.

🏷️ Clause Classification: Detects clause types like Indemnification, Termination, Payment Terms, etc.

⚠️ Risk Rating: Each clause is rated as High, Medium, or Low risk using legal heuristics and BERT-based insights.

✨ Summarization: Generates concise summaries for lengthy clauses using BART transformer.

📊 Interactive Dashboard: Visualizes risk breakdown with bar and donut charts, and exports results to JSON or CSV.

🔒 User Management Dashboard
👤 Secure Authentication: Username, password (hashed), and CAPTCHA-based login/registration.

🧠 Password Analysis: Detects and highlights reused passwords across users.

🔁 Login Tracking: Shows total logins, last login time, and recent activity.

📈 Visual Insights: Tabs for reused password frequency, user growth, and login activity trends.

🧠 Tech Stack
Frontend: Streamlit (with custom theming and UI elements)

NLP & ML:

BERT — Sentence embeddings

BART — Summarization model (facebook/bart-large-cnn)

spaCy — Named Entity Recognition & sentence segmentation

Random Forest & TF-IDF — Extractive summarization fallback

Libraries: Transformers, Torch, Scikit-learn, NLTK, pdfminer.six, docx2txt, pandas, plotly, pymongo

Database: MongoDB (Atlas)

🚀 Setup Instructions
Clone the Repository

bash
Copy
Edit
git clone https://github.com/your-username/corporate-clause-risk-analyzer.git
cd corporate-clause-risk-analyzer
Install Required Packages

bash
Copy
Edit
pip install -r requirements.txt
Download spaCy English Model

bash
Copy
Edit
python -m spacy download en_core_web_sm
Add Environment Variables

Create a .env file and add your MongoDB URI:

ini
Copy
Edit
MONGO_URI=mongodb+srv://your_user:your_pass@cluster.mongodb.net
Run the App

bash
Copy
Edit
streamlit run bert5.py
📸 Demo Screenshots
(Add screenshots here showing: Upload section, Risk Summary Dashboard, Clause View, User Management tabs.)

🔮 Planned Improvements
📝 Clause rewriting suggestions for high-risk clauses.

📄 Clause-to-clause contract comparison.

🌍 Multilingual support (Spanish, German, etc.).

☁️ Deploy as SaaS with admin panel and access control.

📄 License
© 2025 Advika Gupta. This project is licensed under the MIT License.
You are free to use, modify, and distribute this work — provided proper credit is given and the license notice is retained.
