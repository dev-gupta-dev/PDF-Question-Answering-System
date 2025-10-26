
---

🧠 PDF Question Answering System (Local Model)

This project allows you to ask questions directly from the content of a PDF document — no internet or API key required.
It extracts text from PDFs, creates semantic embeddings, and uses a local Hugging Face model to find answers from relevant text chunks.


---

🚀 Features

🧾 Extracts text from any PDF file

🔍 Retrieves the most relevant paragraphs using semantic search (FAISS)

🤖 Answers questions using local Hugging Face transformer models

⚙️ Runs completely offline (no OpenAI or paid APIs)

💡 Simple and extendable code — ideal for AI learning projects



---

🛠️ Tech Stack

Component	Library / Model

PDF Extraction	PyPDF2
Embeddings	sentence-transformers (all-MiniLM-L6-v2)
Semantic Search	FAISS
Question Answering	transformers (distilbert-base-cased-distilled-squad)
Language	Python 3.x



---

📦 Installation

Clone the repository and install dependencies:

git clone https://github.com/yourusername/pdf-question-answering.git
cd pdf-question-answering
pip install -r requirements.txt

If you don’t have a requirements.txt, create one with:

PyPDF2
sentence-transformers
faiss-cpu
transformers
torch


---

🧩 Usage

1. Place your PDF file in the project directory

Example: document.pdf

2. Example Code

pdf_path = "document.pdf"
question = "What is the main topic of this document?"

answer = ask_pdf_question(pdf_path, question)
print("Answer:", answer)

Output Example:

Answer: The document discusses machine learning and data analysis techniques.


---

🧠 How It Works

1. Extract text → Reads text from all PDF pages


2. Split text → Breaks text into manageable chunks


3. Embed chunks → Converts chunks into numerical embeddings


4. Semantic Search → Finds most relevant parts for your question


5. Answer Extraction → Uses a transformer QA model to extract the exact answer from context




---

🧰 Example Architecture

graph LR
A[PDF Document] --> B[Text Extraction (PyPDF2)]
B --> C[Chunking]
C --> D[Embedding (SentenceTransformer)]
D --> E[FAISS Search]
E --> F[Relevant Context]
F --> G[Question Answering Model]
G --> H[Answer]


---

🧩 Optional Improvements

🔹 Build a Streamlit UI to upload PDFs and ask questions

🔹 Use larger models for better accuracy (roberta-base-squad2)

🔹 Add multi-PDF support

🔹 Cache embeddings for faster repeated queries


---

🪪 License

This project is open-source and available under the MIT License.


---
