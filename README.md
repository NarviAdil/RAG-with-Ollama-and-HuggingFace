# RAG-with-Ollama-and-HuggingFace

# 🔍 Retrieval-Augmented Generation (RAG) on PDFs with Ollama and Hugging Face

This project demonstrates how to extract answers from PDF documents using two different local AI stacks:

1. **Ollama + Mistral + Nomic Embeddings**
2. **Hugging Face Transformers + Sentence Transformers**

It showcases the power of Retrieval-Augmented Generation (RAG) to answer complex questions by combining document understanding, semantic search, and local LLMs — all without using the cloud.

---

📸 Screenshot
![image](https://github.com/user-attachments/assets/6c3ed4d9-fbf0-4c8e-9f43-662747870791)

![image](https://github.com/user-attachments/assets/71c6c15e-2550-49ae-b6f6-3a69c67202f7)

![image](https://github.com/user-attachments/assets/d7cc0da8-204a-4ca6-b40c-17e024df60ae)



---

## 🚀 How It Works

1. **Load PDF**: Use `PyPDF2` to read document pages.
2. **Split Text**: Use `RecursiveCharacterTextSplitter` from LangChain.
3. **Embed Chunks**:
   - Ollama version uses `nomic-embed-text`
   - Hugging Face version uses `all-MiniLM-L6-v2` from Sentence Transformers
4. **Store in VectorDB**: FAISS used for semantic similarity search.
5. **Query LLM**:
   - Ollama version uses `mistral` model locally.
   - Hugging Face version uses `mistralai/Mistral-7B-Instruct-v0.1` or any other local LLM.

---

## 🧪 Sample Use Case

> 📄 PDF: *ServiceNow Commercials.pdf*  
> ❓ Question: *What are the customer, technical, and domain-specific challenges?*  
> 💬 Output: Relevant content extracted directly from the PDF with full context.

---

## ⚙️ Requirements

Install the following packages:

### For Ollama version:
```bash
sudo apt install -y pciutils
curl -fsSL https://ollama.com/install.sh | sh
ollama pull mistral
ollama pull nomic-embed-text

pip install langchain langchain-core langchain-community langchain-ollama faiss-cpu PyPDF2 unstructured[all-docs]  

### For hugging face version :

pip install langchain faiss-cpu transformers sentence-transformers PyPDF2







🧠 Author
Adil Narvi
Conversational AI Developer | Kore.ai | NLP | RAG Architect
LinkedIn
