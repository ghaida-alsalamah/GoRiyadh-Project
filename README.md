# 🌆 GoRiyadh – AI Tourist Guide for Riyadh

## 📌 Overview
**GoRiyadh** is an AI-powered tourist guide that helps users explore Riyadh by providing smart recommendations for hotels, restaurants, and cafes.

The system uses a **Retrieval-Augmented Generation (RAG)** architecture to understand user queries and generate personalized suggestions, along with interactive features like exploration, filtering, and itinerary planning.

---
## 🔗 Live Demo 

https://goriyadh.onrender.com/

---

## 🚀 Features

- 🏨 Recommendations for hotels, restaurants, and cafes
- 🗺️ Explore section with filters (rating, price, district)
- 📊 Data-driven insights from real Riyadh datasets
- 🧠 AI-generated responses using LLM
- 🔍 Smart search using natural language (e.g., *“cheap cafes in Olaya”*)
- 📅 Basic itinerary generation based on user preferences
- 🌐 Interactive frontend with modern UI

---

## 🧠 System Architecture

The project follows a **RAG (Retrieval-Augmented Generation)** pipeline:

1. User sends a query  
2. Query is converted into embeddings  
3. Relevant places are retrieved using FAISS  
4. Retrieved data is passed to an LLM  
5. Final response is generated and returned to the user  

---

## ⚙️ Tech Stack

### 🔹 Backend
- FastAPI – API development  
- Uvicorn – ASGI server  

### 🔹 RAG Engine
- Embeddings: Sentence Transformers (`all-MiniLM-L6-v2`)  
- Vector Search: FAISS  
- LLM: Groq (`llama-3.3-70b-versatile`)  

### 🔹 Frontend
- HTML  
- CSS  
- JavaScript  

### 🔹 Data Processing
- Pandas  

### 🔹 Deployment
- Render (Backend hosting)

---

## 📊 Datasets

The system is built using real datasets from Riyadh:

- 🏨 Hotels dataset  
- 🍽️ Restaurants dataset (~19K records after filtering)  
- ☕ Cafes dataset (~2.6K records)

Data preprocessing includes:
- Cleaning and normalization  
- Filtering low-quality entries  
- Merging into a unified structure (name, rating, price, district, description)

---

## 📁 Project Structure

## 📁 Project Structure

```
GoRiyadh/
│
├── api.py                # FastAPI endpoints
├── rag_engine.py        # RAG logic (FAISS + LLM)
├── data_loader.py       # Data preprocessing
├── fetch_images.py      # Image handling
├── requirements.txt
│
├── frontend/            # UI (HTML/CSS/JS)
│   ├── index.html
│   ├── app.js
│   └── style.css
│
├── index.faiss          # Vector index
├── metadata.pkl         # Data mapping
│
└── datasets/
```
--

## ▶️ How to Run

### 1. Install dependencies
```bash
pip install fastapi uvicorn python-multipart
```

### 2. Run backend
```
uvicorn api:app --reload
```

### 3. Open application
- API Docs: http://localhost:8000/docs  
- Frontend: Open frontend/index.html

---

## 💡 Example Queries

- “Best cafes in Riyadh under 50 SAR”  
- “Luxury hotels near King Fahd Road”  
- “Plan a 2-day trip in Riyadh”  

---

## 👥 Team Members

- Ghaida Alsalamah  
- Layan Alsulaiman  
- Lama Faden  
- Muneera Alsaeed  
- Sara Alhamdan  

---

## 🔮 Future Work

- Add booking integration  
- Improve recommendation accuracy  
- Add map-based navigation  
- Personalization based on user behavior  

---

## 📌 Notes

This project demonstrates the use of AI, RAG systems, and data-driven recommendations in a real-world tourism application.
