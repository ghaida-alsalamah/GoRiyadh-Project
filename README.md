# 🌆 GoRiyadh – AI Tourist Guide for Riyadh

## 📌 Overview
**GoRiyadh** is an AI-powered tourist guide designed to help users explore Riyadh efficiently.  
It provides smart recommendations for hotels, restaurants, and cafes using a **Retrieval-Augmented Generation (RAG)** system combined with real-world datasets.

---

## 🚀 Features

- 🏨 Personalized recommendations for hotels, restaurants, and cafes
- 🗺️ Explore section with filters (rating, price, district)
- 🧠 AI-generated responses using a large language model (LLM)
- 🔍 Smart search using natural language (e.g., *“cheap cafes in Olaya”*)
- 📅 Simple itinerary generation based on user preferences
- 🌐 Interactive and responsive user interface

---

## 🧠 System Architecture

The system follows a **RAG (Retrieval-Augmented Generation)** pipeline:

1. User submits a query  
2. Query is converted into embeddings  
3. Relevant data is retrieved using FAISS  
4. Retrieved results are passed to the LLM  
5. Final response is generated and returned  

---

## ⚙️ Tech Stack

### 🔹 Backend
- FastAPI  
- Uvicorn  

### 🔹 RAG Engine
- Sentence Transformers (`all-MiniLM-L6-v2`)  
- FAISS (Vector Search)  
- Groq LLM (`llama-3.3-70b-versatile`)  

### 🔹 Frontend
- HTML  
- CSS  
- JavaScript  

### 🔹 Data Processing
- Pandas  

### 🔹 Deployment
- Render  

---

## 📊 Datasets

The project uses real datasets from Riyadh:

- 🏨 Hotels dataset  
- 🍽️ Restaurants dataset (~19K records after filtering)  
- ☕ Cafes dataset (~2.6K records)

### Data Processing Steps:
- Data cleaning and normalization  
- Removing low-quality entries  
- Unifying structure (name, rating, price, district, description)

---

## 📁 Project Structure

GoRiyadh/
│
├── api.py
├── rag_engine.py
├── data_loader.py
├── fetch_images.py
├── requirements.txt
│
├── frontend/
│ ├── index.html
│ ├── app.js
│ └── style.css
│
├── index.faiss
├── metadata.pkl

--

## ▶️ How to Run

### 1. Install dependencies
```bash
pip install fastapi uvicorn python-multipart
### 2. Run backend
uvicorn api:app --reload

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


