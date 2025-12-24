# JuriAssist-AI-Based-Legal-Assistance-System
JuriAssist: Hybrid Quantum-Classical Legal Consultation System

JuriAssist is a high-precision legal retrieval platform that combines traditional Natural Language Processing (NLP) with Grover-inspired Quantum Search simulations. It is designed to navigate the Indian Penal Code (IPC) and provide grounded, hallucination-free legal advice.

🚀 Key Features

Hybrid Retrieval: Combines TF-IDF vectorization with Qiskit-based Quantum Search.

Quantum Search Simulation: Uses a Grover-inspired circuit to prioritize legal matches.

Fuzzy Query Correction: Robust handling of user typos and legal jargon.

Dual Interface: Includes both a Streamlit Web Dashboard and a Tkinter Desktop UI.

Emergency Alerting: Integrated Twilio SMS system for high-severity legal alerts.

🛠️ Tech Stack

Languages: Python 3.8+

Quantum Framework: Qiskit, Qiskit-Aer

Machine Learning: Scikit-Learn, Sentence-Transformers

NLP: NLTK, FuzzyWuzzy

Web Framework: Streamlit

Alert System: Twilio API

🧬 Algorithm Logic

The system follows a three-stage architectural pipeline:

The Backbone (Preprocessing): Normalizes the ipc_sections.csv dataset and converts legal text into a TF-IDF sparse matrix.

The Neck (Classical Scoring): Computes Cosine Similarity between the vectorized user query and the database.

The Head (Quantum Search): Maps classical scores onto a probability distribution within a Quantum Circuit. It applies Hadamard transformations and measures the state through a QasmSimulator (2000 shots) to identify the top-K legal sections.

📁 Project Structure

├── main.py              # Streamlit Web Interface
├── camera.py            # Tkinter Desktop Interface
├── detection.py         # Core Engine (Preprocessing + Quantum Search)
├── mail.py              # Twilio Alerting Logic
├── keys.py              # API Credentials
├── trained_model.pkl    # Serialized K-Means & Embeddings
├── static/
│   └── ipc_sections.csv # Dataset of Indian Penal Code
└── requirements.txt     # Dependency List


⚙️ Installation & Setup

Clone the repository:

git clone [https://github.com/YourUsername/JuriAssist.git](https://github.com/YourUsername/JuriAssist.git)
cd JuriAssist


Install Dependencies:

pip install -r requirements.txt


Configure API Keys:
Create a keys.py file and add your Twilio credentials:

account_sid = 'your_sid'
auth_token = 'your_token'
twilio_number = 'your_twilio_number'
target_number = 'your_phone_number'


Run the Application:

Web App: streamlit run main.py

Desktop App: python camera.py

📊 Performance

Unlike standard Large Language Models (LLMs), JuriAssist ensures 100% factual grounding. By retrieving directly from verified statutes and using quantum probability for ranking, it eliminates AI hallucinations in legal contexts.


🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements.
