# ⚕️ Medical AI RAG Assistant (PubMedQA)

This project implements a complete **Retrieval-Augmented Generation (RAG)** system in the medical domain. It uses a search algorithm to locate relevant medical texts from the PubMed database, and then utilizes an open-source Large Language Model (such as Qwen or Mistral via Hugging Face) to generate accurate and comprehensive summaries.

## 📂 Project Structure

The repository consists of the following main files:

* **`data_exploration_2.ipynb`**: Contains the code for data preparation. It loads the initial `ori_pqal.json` file, cleans the text, concatenates the questions and answers, and exports the ready-to-use `pubmedqa_clean.csv` file.
* **`assistant_2.ipynb`**: Implements the search algorithm (Information Retrieval). It uses `TfidfVectorizer` and `cosine_similarity` from scikit-learn to find the most relevant medical articles based on the user's query.
* **`app_2.ipynb`**: The main application. It integrates the search engine with the **Hugging Face Inference API** and creates a Graphical User Interface (UI) using the **Gradio** library.
* **`data/`**: Directory containing the data:
  * `ori_pqal.json`: The initial raw dataset.
  * `pubmedqa_clean.csv`: The processed and cleaned dataset.

## 🛠️ System Requirements

To run the application locally, make sure you have Python 3.12+ installed along with the following libraries:

```bash
pip install pandas scikit-learn gradio huggingface_hub
