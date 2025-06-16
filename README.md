# RAG Mechanisms Evaluation

This repository provides the source documents, parsed text, and question–answer sets used to evaluate different retrieval mechanisms in Retrieval Augmented Generation (RAG) systems. It supports two data domains—financial reports and news articles—and three distinct question-set types to facilitate a systematic comparison of vector-based (Naïve RAG) and graph-based (GraphRAG) retrieval methods.

## Repository Structure

The repository has the following top-level folders:

- **Docugami**  
  This folder contains the Sec-10-Q subset of corporate quarterly reports.  
  - `pdfs/`  
    Original PDF files of the financial reports.  
  - `parsed/`  
    Marker-PDF-parsed Markdown files, ready for ingestion into indexing pipelines.  
  - `question_sets/`  
    Three sets of 50 questions each:  
    1. **gold_standard/** – Human-verified questions with reference answers.  
    2. **synth_ragas/** – Synthetic questions and answers generated via the RAGAs framework.  
    3. **synth_sense/** – Sensemaking-oriented questions generated following the GraphRAG study protocol.

- **Multihop-RAG**  
  This folder contains the news-article corpus and corresponding question sets.  
  - `corpus.json`  
    The original JSON file with 609 news articles and metadata fields.  
  - `parsed/`  
    Markdown-formatted text files extracted from each article.  
  - `question_sets/`  
    Two sets of 50 questions each:  
    1. **synth_ragas/** – Synthetic questions and answers from the RAGAs testset generator.  
    2. **synth_sense/** – Global sensemaking questions following the GraphRAG methodology.

## Data Sources

This project makes use of two publicly available corpora:

- **Sec-10-Q Financial Reports Subset** from the Docugami KG-RAG Datasets.  
  Source: [https://github.com/docugami/KG-RAG-datasets  ](https://github.com/docugami/KG-RAG-datasets/tree/main/sec-10-q)
  We gratefully acknowledge the Docugami team for providing this collection of quarterly reports.

- **Multihop-RAG News Corpus** by Tang et al.  
  Source: [https://github.com/tangyudi/Multihop-RAG  ](https://github.com/yixuantt/MultiHop-RAG/tree/main/dataset)
  We thank Yudi Tang and collaborators for releasing this 609-article dataset.

Each dataset was used under its original license and with appreciation for the effort of its maintainers.


## Citation

If you make use of this repository in your research, please cite our thesis and the two datasets as follows:

```bibtex
@mastersthesis{hoffmann2025comparative,
  author       = {Oscar Hoffmann and Fredrik Ramberg},
  title        = {{A Comparative Study of Naïve RAG and GraphRAG: Evaluation Insights and Performance-Cost Trade-Offs in Retrieval Augmented Generation}},
  school       = {Linköping University, Department of Computer and Information Science},
  year         = {2025},
  type         = {Master’s thesis}
}
