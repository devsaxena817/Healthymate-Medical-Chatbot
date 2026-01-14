# 🩺 HealthyMate – Medical Chatbot

HealthyMate is an AI-powered medical chatbot designed to provide **basic health guidance, symptom understanding, and medical information** in a simple, user-friendly way. It aims to assist users with preliminary health-related queries while clearly encouraging consultation with qualified healthcare professionals.

---

## 🚀 Features

* 🤖 AI-based conversational medical assistant
* 📝 Symptom analysis and health guidance
* 💊 General information about diseases, medications, and wellness
* 🧠 Context-aware responses using LLMs
* 🌐 Web-based interactive interface (Streamlit)
* 🔐 User-friendly and privacy-conscious design

> ⚠️ **Disclaimer**: HealthyMate is **not a replacement for professional medical advice**. Always consult a certified doctor for diagnosis or treatment.

---

## 🛠️ Tech Stack

* **Frontend**: Streamlit
* **Backend / AI**: Python, LangChain / LangGraph
* **LLM**: OpenAI / compatible LLM APIs
* **Database (optional)**: SQLite / Vector DB (FAISS / Chroma)
* **Environment**: Python 3.9+

---

## 📂 Project Structure

```
HealthyMate/
│
├── data/                   # Dataset & notebooks used for testing
├── research/               # Research experiments & analysis
├── src/                    # Core chatbot logic & modules
├── static/                 # Static files (CSS, images)
├── templates/              # HTML templates for web app
│
├── app.py                  # Main web application entry point
├── store_index.py          # Vector store / index creation script
├── requirements.txt        # Project dependencies
├── setup.py                # Package setup configuration
├── template.sh             # Shell script for setup/automation
├── .gitignore              # Ignored files
├── LICENSE                 # License file
├── README.md               # Project documentation
└── readme.md               # Backup / merged README
```

HealthyMate/
│
├── app.py                  # Main Streamlit application
├── chatbot/                # Chatbot logic
│   ├── prompts.py          # System & medical prompts
│   ├── model.py            # LLM initialization
│   └── graph.py            # LangGraph flow
│
├── data/                   # Medical knowledge / embeddings
├── utils/                  # Helper functions
├── requirements.txt        # Dependencies
├── .env                    # API keys (not committed)
└── README.md               # Project documentation

````

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/HealthyMate.git
cd HealthyMate
````

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate      # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Environment Variables

Create a `.env` file and add:

```env
OPENAI_API_KEY=your_api_key_here
```

---

## ▶️ Run the Application

```bash
streamlit run app.py
```

Open your browser at:

```
http://localhost:8501
```

---

## 💬 Example Use Cases

* Understanding symptoms like fever, headache, cough
* General disease information (diabetes, hypertension, flu, etc.)
* Medication awareness (usage & precautions)
* Wellness tips and lifestyle guidance

---

## 🔒 Safety & Ethics

* No medical diagnosis is claimed
* Encourages professional consultation
* Avoids emergency decision-making
* Designed with responsible AI guidelines

---

## 📌 Future Enhancements

* 🧾 Medical report upload & summarization
* 🗣️ Voice-based interaction
* 🌍 Multi-language support
* 🧠 Personal health history tracking
* 🔗 Doctor & hospital recommendation system

---

## 👨‍💻 Contributors

* **Developer**: Dev Saxena

---

## 📜 License

This project is licensed under the **MIT License**.

---

## ⭐ Acknowledgements

* OpenAI
* Streamlit
* LangChain / LangGraph community

---

If you find this project helpful, don’t forget to ⭐ the repository!
