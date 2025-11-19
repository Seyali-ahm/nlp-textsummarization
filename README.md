# Text Summarization Pipeline  
**Author:** Seyyed Ali Ahmadi  
[GitHub Profile](https://github.com/Seyali-ahm)  
[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

---

## 📘 Project Overview  
This repository contains a modular pipeline for **automatic text summarization** using modern NLP techniques. The system supports both _extractive_ and _abstractive_ summarization workflows, leveraging pretrained transformer models and custom post-processing to generate concise summaries of longer documents.

The goal of this project is to enable researchers and engineers to apply summarization methods out-of-the-box, as well as adapt and extend the pipeline for domain-specific tasks, such as legal, medical or news summarization.

---

## 🎯 Motivation  
With the ever-increasing volume of textual content published online every day, the ability to quickly extract key insights from long documents is more important than ever.  
This project addresses that need by providing a pipeline that allows you to:  
- Convert long text documents into high-quality summaries  
- Choose between faster extractive methods or more nuanced abstractive methods  
- Deploy models for inference in research or production settings  

---

## 🧩 Dataset & Scope  
For demonstration purposes, the pipeline was developed using publicly available datasets and transformer-based models.  
- Example data: news articles, blog posts, technical reports  
- Supported summarization types:  
  - **Abstractive**: Generates entirely new sentences to capture the core meaning  

The repository includes sample notebooks and pre-processing scripts to help you adapt to your own data.

---

## ⚙️ Pipeline Architecture  
1. **Pre-processing**  
   - Tokenization, sentence segmentation  
   - Stop-word removal and optional stemming/lemmatization  
   - Padding/truncation for transformer input  
2. **Embedding / Feature Extraction**  
   - For extractive: uses sentence embeddings (e.g., from Sentence-Transformers)  
   - For abstractive: uses encoder-decoder architectures (e.g., T5, BART)  
3. **Summarization**  
   - Extractive: ranking and selection of top-k sentences  
   - Abstractive: fine-tuned model generates new summary text  
4. **Post-processing**  
   - Clean up redundant sentences  
   - Adjust length based on user configuration (e.g., ratio or fixed length)  
5. **Evaluation**  
   - Provides ROUGE scores and other summary-quality metrics  

---

## 🧠 Example Model Configuration  

| Task Type        | Model                | Summary Length      |
|------------------|----------------------|----------------------|
| Abstractive       | Google Pegasus              | Maximum 128 tokens    |


---


## 🧰 Technology Stack  
- Python 3.10+  
- Hugging Face Transformers  
- Sentence-Transformers  
- PyTorch / TensorFlow backend  
- NLTK / SpaCy (for tokenization & preprocessing)  
- YAML (for configuration)  
- Jupyter Notebooks (for experimentation)  
- Docker (optional for deployment)  

---

## 🚀 Getting Started  
```bash
# Clone the repository
git clone https://github.com/Seyali-ahm/nlp-textsummarization.git
cd nlp-textsummarization

# (Optional) create a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run a demo script using default config
python src/run_summary.py --input data/sample_text.txt --config config.yaml
```

---

## 📂 Project Structure  
```
nlp-textsummarization/
│
├── data/                     ← sample input files  
├── config.yaml               ← default configuration file  
├── notebooks/                ← exploratory analysis and visualization  
├── src/
│   ├── preprocessing/        ← tokenization, sentence splitting  
│   ├── extractive/           ← extractive summarizer code  
│   ├── abstractive/          ← abstractive summarizer code  
│   ├── evaluation/          ← scripts for ROUGE and metrics  
│   └── run_summary.py       ← CLI entry point  
│
├── requirements.txt  
└── README.md                ← this file  
```

---

## 🔬 Future Work  
- Add support for **multi-document summarization**  
- Integrate **query-based summarization** (user asks a question, model summarises accordingly)  
- Experiment with **domain-specific fine-tuning** (legal, medical)  
- Provide a **web-service UI** for interactive summarization  
- Optimize for **real-time summarization** with quantized models  

---

### 🙏 Acknowledgements  
Thanks to the open-source NLP community and contributors to Hugging Face, Sentence-Transformers, and related libraries.

---

*This project represents my work in natural‐language processing and summarization engineering.*  
Feel free to explore, adapt, and extend it for your own needs!
