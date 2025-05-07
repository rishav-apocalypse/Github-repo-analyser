# Github-repo-analyser

##  About This Project

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline using the **[Agno](https://docs.agno.com/introduction)** framework. It pulls GitHub issues, generates sentence embeddings, stores them in **LanceDB**, and summarizes patterns using **Gemini** via Agno’s agent interface.

---

##  Installation

Make sure you have Python 3.9+ installed. Then, install the required libraries using the following:
-pip install agno
-pip install lancedb
-pip install sentence-transformers
-pip install pygithub

**Also input Gemini API key and Github where requested**

## 🔧 Tools & Libraries Used

- **Agno** – for agent orchestration, vector storage, and LLM integration  
- **Sentence Transformers** – for custom embedding generation  
- **LanceDB** – for fast vector similarity search  
- **Gemini (via Agno)** – for summarizing issues and extracting insights  
- **PyGitHub** – to fetch and interact with GitHub issues  

---

## Developer Notes

While Agno is a powerful framework with many built-in capabilities, working with it came with a few pain points:

- **Lack of clear documentation**: Finding updated attribute names and APIs was time-consuming.  
- **Tight coupling** of components like `AgentKnowledge`, `LanceDb`, and `Document` made debugging harder.  
- **Embedding pipeline felt abstracted away**, where using sentence-transformers and LanceDB directly could have been easier and more transparent.  
- Compared to **LangChain**, Agno currently lacks the developer ergonomics and discoverability that make building pipelines smooth.

That said, Agno shows potential—especially for rapidly building agent-driven apps—and this project is a step toward exploring its full capabilities.

