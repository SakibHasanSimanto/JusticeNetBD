# JusticeNet-BD: A RAG-Based Legal Assistant for Women in Bangladesh 🇧🇩⚖️

**JusticeNet-BD** is an experimental legal assistant tool designed to make legal information more accessible for women in Bangladesh. Built using Retrieval-Augmented Generation (RAG), this Streamlit app retrieves relevant legal knowledge from a curated corpus and generates responses to user queries. 

Kindly **Read the model's research paper** to learn about model architecture, usability, and performance against SOTA models (Gemini Flash 2.5, ChatGPT-4o Turbo, and DeepSeek-V3).

🌐 **Live App:** [https://justice-net-bd.streamlit.app/](https://justice-net-bd.streamlit.app/)

---

## 🔍 Project Overview

This assistant is tailored to answer questions related to Bangladeshi laws concerning women's rights and protection — such as the **Penal Code**, **Nari o Shishu Nirjatan Daman Ain 2000**, **Dowry Prohibition Act** etc. It uses a custom RAG pipeline to retrieve legal content and generate answers grounded in actual legal clauses. The data is incremented weekly to boost model performance. 

---

## 📸 Demo & Screenshots
Below are some screenshots demonstrating the usage of JusticeNetBD:

<p align="center"> <img src="https://github.com/SakibHasanSimanto/JusticeNetBD/blob/main/ss1.png" alt="Screenshot 1" width="600"/> <br/><em>Figure 1: Home Page Interface</em> </p> <p align="center"> <img src="https://github.com/SakibHasanSimanto/JusticeNetBD/blob/main/ss2.png" alt="Screenshot 2" width="600"/> <br/><em>Figure 2: Introduction</em> </p> <p align="center"> <img src="https://github.com/SakibHasanSimanto/JusticeNetBD/blob/main/ss3.png" alt="Screenshot 3" width="600"/> <br/><em>Figure 3: Legal Query Sent by User</em> </p> <p align="center"> <img src="https://github.com/SakibHasanSimanto/JusticeNetBD/blob/main/ss4.png" alt="Screenshot 4" width="600"/> <br/><em>Figure 4: Resource Link Suggestions</em> </p> <p align="center"> <img src="https://github.com/SakibHasanSimanto/JusticeNetBD/blob/main/ss5.png" alt="Screenshot 5" width="600"/> <br/><em>Figure 5: Another Legal Query Sent by User</em> </p> 

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

--- 

## ⚠️ Disclaimer 
This is an experimental tool intended for informational purposes only. It only helps you search and gather relevant legal information according to your queries. It cannot provide professional legal assistance.

## 🛠️ Reproducibility and Deployment Guidelines for Developers

To reproduce or deploy your own version of the JusticeNet-BD assistant, or any RAG Assistant, you will need **four essential files** hosted in a public GitHub repository:

- `chunks.pkl` — the preprocessed vector-ready text chunks from your legal corpus.
- `chunks.faiss` — the FAISS index generated from the embeddings of the chunks.
- `app.py` — the main application script (written in Streamlit).
- `requirements.txt` — the dependency file listing all Python packages used.

> 📝 **Note:** Both `chunks.pkl` and `chunks.faiss` are generated from your own text corpus (e.g., `your_corpus.txt`). For coherent chunking, ensure that **each paragraph in the corpus contains a complete and self-contained piece of information**.

---

### 📓 Colab Notebook for File Generation

To generate the required files, follow this guided Google Colab notebook:

👉 [Files required for RAG system](https://colab.research.google.com/drive/1l_18wbRGooj1Omq2q1S7YB98NddYU1k2?usp=sharing)

This notebook walks you through:

- Reading a `.txt` legal corpus.
- Creating paragraph-wise chunks.
- Embedding the chunks using SentenceTransformers.
- Creating and saving the `.pkl` and `.faiss` files.
- Writing app.py file.
- Creating requirements.txt.

---

### 🚀 Deploying to Streamlit Cloud

Once your files are ready and uploaded to a **public GitHub repository**:

1. Visit [share.streamlit.io](https://share.streamlit.io)
2. Click **"Create a new app"**
3. Choose the GitHub repo that contains your `app.py`
4. Follow the UI prompts to complete deployment.
5. Then, click on **Advanced Settings**. 

---

### 🔑 API Configuration (GROQ LLM)

To use the GROQ LLM for generating answers, you'll need to add your API key as a **secret variable** in Streamlit Cloud.

✅ You **do not need** to upload a `.toml` file or edit your GitHub repo.

Instead, follow these steps:

1. After selecting your GitHub repo in [share.streamlit.io](https://share.streamlit.io), go to the **"Advanced Settings"** section.
2. Scroll to the **"Secrets"** field.
3. Add the following line:
   GROQ_API_KEY = "your_api_key"

Click "Deploy" or "Save" — your app will now have access to the API key via `st.secrets["GROQ_API_KEY"]`.

🔗 Get your free GROQ API key from: [https://console.groq.com/home](https://console.groq.com/home)

> ⚠️ Note: The free tier has usage limits, but resets automatically after overuse.



