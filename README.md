# 🎥 TubeSage — Ask Questions from YouTube Videos

**TubeSage** is an AI-powered web application that lets you ask questions directly from any YouTube video and receive accurate, context-aware answers based strictly on the video’s transcript.

Instead of manually watching long videos, TubeSage extracts the transcript, retrieves the most relevant segments using semantic search, and applies a Retrieval-Augmented Generation (RAG) pipeline to answer your questions reliably.

👉 **Live App:**  
🔗 https://ragtube-vansh.streamlit.app/

---

## ✨ Features

- 📌 Ask natural-language questions about YouTube videos  
- 🧠 Answers generated only from the video transcript (no hallucinations)  
- 🌐 Supports **English and Hindi** transcripts  
- 🗣 Answers in the **same language as the user’s question**  
- ⚡ Fast semantic search using FAISS  
- 🎨 Clean and simple Streamlit UI  

---

## 🔧 How It Works

1. User provides a YouTube video URL and a question  
2. The app fetches the transcript using the YouTube Transcript API  
3. The transcript is split into chunks and embedded  
4. FAISS retrieves the most relevant transcript segments  
5. A Gemini-based LLM generates an answer using only the retrieved context  

This ensures responses are **accurate, grounded, and explainable**.

---

## 🛠 Tech Stack

- **Python**
- **Streamlit**
- **LangChain (Runnables API)**
- **Google Gemini (LLM)**
- **FAISS** (vector similarity search)
- **Hugging Face Sentence Transformers**
- **YouTube Transcript API**

---

## 🚀 Getting Started (Local Setup)

### 1️⃣ Clone the repository
```bash
git clone https://github.com/your-username/tubesage.git
cd tubesage
```

### 2️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

### 3️⃣ Set environment variables
Create a `.env` file in the project root:
```env
HF_TOKEN=your_huggingface_token
GOOGLE_API_KEY=your_google_gemini_api_key
```

### 4️⃣ Run the app
```bash
streamlit run app.py
```

---

## 🎯 Use Cases

- Studying long lectures and tutorials  
- Quickly extracting explanations from tech videos  
- Learning from multilingual educational content  
- Understanding real-world RAG pipeline implementation  

---

## 📌 Notes

- The app answers **only from the transcript context**
- If the answer is not present in the video, it responds with **"I don't know."**
- This project demonstrates a **production-style RAG architecture**

---

## 📄 License

This project is open-source and available under the MIT License.

---

### ⭐ If you find this project useful, consider starring the repository!
