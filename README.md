# LangChain RAG Chatbot 🧠📚

This project demonstrates a Retrieval-Augmented Generation (RAG) pipeline using LangChain, OpenAI, and ChromaDB. The goal is to answer user questions contextually using a vector database built from custom `.docx` lecture notes.

## 🚀 Features

- 📝 Loads `.docx` lecture notes using `Docx2txtLoader`
- 🔍 Splits text using markdown headers and character-based chunking
- 🧠 Embeds documents with OpenAI `text-embedding-ada-002`
- 📦 Stores embeddings in Chroma vector database
- 🔁 Retrieves relevant context via MMR (Maximal Marginal Relevance)
- 💬 Generates contextual responses using GPT-4
- 🧾 Automatically includes the source lecture title for transparency

## 🧱 Tech Stack

- [LangChain](https://www.langchain.com/)
- [OpenAI GPT-4](https://platform.openai.com/)
- [Chroma VectorDB](https://www.trychroma.com/)
- [Python 3.11+](https://www.python.org/)
- [Docx2txt](https://pypi.org/project/docx2txt/)

## 📁 Project Structure

- RAG_Project.ipynb  # Main notebook demonstrating RAG pipeline
- ./intro-ds-vectorstore/ # Directory where the vectorstore is persisted
- Introduction_to_Data_and_Data_Science_2.docx #  lecture note input
- Make sure to add your OpenAI key in a .env file:  OPENAI_API_KEY=your_key_here

## 🧪 How It Works

The notebook loads and cleans .docx lecture notes.

It splits the content into meaningful chunks using markdown headers and sentence-based logic.

The chunks are embedded and stored in a persistent Chroma vectorstore.

On receiving a user query, relevant documents are retrieved based on semantic similarity.

The GPT-4 model answers the question using only the retrieved context.

The output ends with the name of the relevant lecture as the source.

## 🧠 Sample Prompt

Which programming language do data scientists use?

Sample Output:

Python is the most commonly used programming language in data science due to its rich ecosystem of libraries and community support.

Resources: Introduction to Programming for Data Science

## 🧩 TODOs / Improvements

Add a Streamlit or Gradio UI

Support PDF and web-based loaders

Improve chunking strategy with overlap

Allow multi-document indexing

## 👨‍💻 Author
Aung Kaung Pyae Paing – AI/ML Enthusiast
