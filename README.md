# Natural Language Processing Lab

This workspace contains 10 lab assignments for the NLP course (Semester 5, B.Tech AI). Each lab is self-contained, but some labs reuse outputs from earlier labs.

## Course Information

- Subject: Natural Language Processing
- Semester: 5
- Degree: B.Tech Engineering
- Branch: Artificial Intelligence

## Repository Structure

```
Lab1/  Tokenization (Hindi and Marathi)
Lab2/  DFA and morphological FST
Lab3/  Trie-based stemming and frequency analysis
Lab4/  N-gram language models and smoothing
Lab5/  Good-Turing smoothing and deleted interpolation
Lab6/  Katz backoff, Kneser-Ney, sentence generation
Lab7/  PMI, TF-IDF, nearest neighbors
Lab8/  Naive Bayes text classification
Lab9/  Subword tokenization (BPE, WordPiece)
Lab10/ POS tagging with HMM + Viterbi
```

## Lab Details and Entry Points

### Lab 1: Tokenization
- Main file: `Lab1/tokenizer.ipynb`
- Outputs: tokenized Hindi/Marathi sentence and token JSON files
- Notes: Uses the HuggingFace `datasets` package for the IndicCorpV2 corpus

### Lab 2: DFA and Morphology (FST)
- Scripts: `Lab2/dfa1.py`, `Lab2/dfa2.py`
- Outputs: `dfa1_output.txt`, `dfa2_output.txt`, Graphviz diagrams
- Dependencies: `automathon`, `graphviz`

### Lab 3: Trie Stemming and Frequency Analysis
- Scripts: `Lab3/trie_stemming.py`, `Lab3/frequency_analysis.py`
- Outputs: `prefix_out.txt`, `suffix_out.txt`, `trie_q1_output.txt`
- Notes: Frequency analysis reads `Lab1/tokenized_hindi_tokens.json`

### Lab 4: N-gram Language Models
- Scripts: `Lab4/LanguageModels.py`, `Lab4/smoothing.py`, `Lab4/application.py`
- Outputs: Hindi/Marathi unigram to quadragram TSVs and smoothing results
- Notes: Reads `Lab1/tokenized_hindi_tokens.json` and `Lab1/tokenized_marathi_tokens.json`

### Lab 5: Good-Turing Smoothing
- Script: `Lab5/Good_Turing.py`
- Notes: Loads data from `Lab1/tokenized_hindi_sentences.json` or `Lab4/news_articles.txt`

### Lab 6: Advanced Smoothing and Generation
- Scripts: `Lab6/katz_backoff.py`, `Lab6/kneser_ney.py`, `Lab6/sentence_generation.py`
- Outputs: Models and generated sentences under `Lab6/results/`
- Notes: Requires the TSV n-gram files produced in Lab 4

### Lab 7: PMI, TF-IDF, Nearest Neighbors
- Scripts: `Lab7/pmi.py`, `Lab7/tf-idf.py`, `Lab7/nearest_neighbour.py`
- Outputs: PMI CSVs, TF-IDF matrices, nearest neighbor files
- Notes: Uses tokenized data from Lab 1 and models from Lab 4

### Lab 8: Naive Bayes Classification
- Scripts: `Lab8/naive_bayes.py`, `Lab8/naive_bayes_detailed_analysis.py`
- Notes: Demonstrates feature engineering and classification on a small text dataset

### Lab 9: Subword Tokenization
- Script: `Lab9/bpe.py`
- Notes: Implements BPE and WordPiece with multilingual pre-tokenization

### Lab 10: POS Tagging
- Script: `Lab10/pos.py`
- Data: `Lab10/wsj_pos_tagged_en.txt`
- Notes: HMM with Viterbi decoding and 5-fold cross-validation

## How to Run

Use Python 3 from the repository root. Examples:

```bash
# Lab 2
python Lab2/dfa1.py
python Lab2/dfa2.py

# Lab 4
python Lab4/LanguageModels.py

# Lab 6
python -c "from Lab6.katz_backoff import main; main(['hindi'], num_sentences=100)"
python -c "from Lab6.kneser_ney import main; main(['hindi'], num_sentences=100)"
```

Some labs require additional Python packages (see each lab README for details).

## Notes

- This repository is maintained for academic and learning purposes.
- If you generate outputs, they are written into the corresponding lab folder.

## Author

Smit
B.Tech Artificial Intelligence Student