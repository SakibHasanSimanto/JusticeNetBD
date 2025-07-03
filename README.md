# JusticeNet-BD: A RAG-Based Legal Assistant for Women in Bangladesh 🇧🇩⚖️

**JusticeNet-BD** is an experimental legal assistant tool designed to make legal information more accessible for women in Bangladesh. Built using Retrieval-Augmented Generation (RAG), this Streamlit app retrieves relevant legal knowledge from a curated corpus and generates responses to user queries. 
Kindly **Read the model's research paper** to learn about model architecture, usage guidelines, and security concerns.

🌐 **Live App:** [https://justice-net-bd.streamlit.app/](https://justice-net-bd.streamlit.app/)

---

## 🔍 Project Overview

This assistant is tailored to answer questions related to Bangladeshi laws concerning women's rights and protection — such as the **Penal Code**, **Nari o Shishu Nirjatan Daman Ain 2000**, **Dowry Prohibition Act** etc. It uses a custom RAG pipeline to retrieve legal content and generate answers grounded in actual legal clauses. The data is incremented weekly to boost model performance. 

---

## 📁 Repository Structure

| File | Description |
|------|-------------|
| `app.py` | Main application logic written in Streamlit |
| `bdWomanLaw_chunks.pkl` | Preprocessed chunks from the legal corpus |
| `bdWomanLaw_index.faiss` | FAISS vector index for document retrieval |
| `women_rag_corpus1.txt` | Primary knowledge base (updated weekly) |
| `requirements.txt` | Python dependencies required to run the app |

## 📚 Knowledge Base Updates 
The legal corpus (women_rag_corpus1.txt) is updated regularly to reflect changes or additions in relevant laws and services. After updates, bdWomanLaw_chunks.pkl and bdWomanLaw_index.faiss are regenerated accordingly.

## ⚠️ Disclaimer 
This is an experimental tool intended for informational purposes only. It only helps you search and gather relevant legal information according to your queries. It cannot provide professional legal assistance.
