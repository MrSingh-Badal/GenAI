# GenAI

Lightweight examples showing how to connect to local/hosted LLMs and embeddings using LangChain adapters (Hugging Face, Mistral). Includes small demo scripts for chat and embedding workflows to help you experiment quickly.

## Stack
- Language(s): Python 3.8+
- Framework / runtime: plain Python scripts using LangChain adapters
- Notable libraries: langchain, langchain-mistralai, langchain_huggingface, python-dotenv

## What’s in this repo
- chatmodels/
  - Huggingface.py        — demo: Chat via LangChain Hugging Face endpoint
  - chatbot.py            — interactive console chatbot using ChatMistralAI
- embeddingmodels/
  - huggingfacae_embeddding.py — demo: create sentence embeddings via Hugging Face
- requirements.txt        — dependency list used by examples

## Quickstart (short path)
1. Clone
   git clone https://github.com/MrSingh-Badal/GenAI.git
   cd GenAI

2. Create virtual environment and install
   python -m venv .venv
   source .venv/bin/activate   # Windows: .venv\Scripts\activate
   python -m pip install --upgrade pip
   pip install -r requirements.txt

3. Add credentials
   - Create a `.env` file in the repo root to store any provider keys you need.
   - Common variables the examples may require:
     - HUGGINGFACEHUB_API_TOKEN (Hugging Face Hub token) or other HF credentials
     - Any Mistral or other provider keys required by your LangChain adapters
   - Example `.env` (do not commit real keys):
     HUGGINGFACEHUB_API_TOKEN=your_token_here

## Running the demos

- Interactive Mistral chatbot
  - File: chatmodels/chatbot.py
  - Usage:
    python chatmodels/chatbot.py
  - The script asks you to choose a mode (angry / funny / sad) then enters an interactive loop where you can chat. Type `0` to exit.

- HuggingFace chat demo
  - File: chatmodels/Huggingface.py
  - Usage:
    python chatmodels/Huggingface.py
  - This script shows a minimal use of a Hugging Face endpoint via LangChain.

- Embeddings demo
  - File: embeddingmodels/huggingfacae_embeddding.py
  - Usage:
    python embeddingmodels/huggingfacae_embeddding.py
  - Produces embeddings for a small hard-coded list of texts.

## Notes & suggestions
- These scripts are minimal demos for learning and exploration. They:
  - Rely on environment variables and the python-dotenv loader.
  - Do not include robust error handling or input validation.
- Minor issues to consider fixing:
  - File name typos: `huggingfacae_embeddding.py` has spelling inconsistencies; consider renaming to `huggingface_embedding.py`.
  - Add a `.env.example` with the variables you expect.
  - Pin exact versions in `requirements.txt` for reproducibility.
  - Add a proper LICENSE file and CONTRIBUTING guide if you want others to collaborate.
  - Add docstrings and comments inside scripts to explain expected env vars and credentials.

## Contributing
Contributions and improvements are welcome. Suggested first PRs:
- Add `.env.example`
- Fix filename typos and update README usage
- Add error handling and logging to the demo scripts



