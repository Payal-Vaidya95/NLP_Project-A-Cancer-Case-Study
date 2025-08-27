# NLP_Project-A-Cancer-Case-Study
# 🧬 Automated Biomedical Text Processing Using NLP – A Cancer Case Study

This project presents a full-stack biomedical NLP pipeline designed to extract, retrieve, and classify clinical cancer descriptions from unstructured medical text. Developed during my graduate studies in Health Informatics at Rutgers University, it integrates preprocessing, named entity recognition (NER), semantic search, and transformer-based classification to support clinical decision-making.

## 📌 Objectives

- Clean and standardize biomedical text using NLP preprocessing techniques  
- Extract CHEMICAL and DISEASE entities using domain-specific NER models  
- Retrieve semantically relevant cancer descriptions using BERT-based embeddings  
- Classify cancer types (lung, colon, thyroid) using a fine-tuned DistilBERT model  

## 🧪 Methodology

### Preprocessing  
- Lowercasing, lemmatization, stopword and duplicate removal  
- Reduced dataset from 7,569 to 996 unique clinical descriptions  

### Named Entity Recognition (NER)  
- Models: BC5CDR and BIONLP13CG via SciSpacy  
- BC5CDR achieved F1-scores of 0.96 (CHEMICAL) and 0.97 (DISEASE)  
- BIONLP13CG showed lower precision and recall, confirming BC5CDR’s clinical specificity  

### Semantic Information Retrieval  
- Sentence-BERT embeddings with cosine similarity  
- Best performance on treatment-related queries (Precision = 1.0)  
- Lower scores for symptom-based queries, suggesting need for domain-tuned models  

### Text Classification  
- Fine-tuned DistilBERT to predict cancer type from clinical descriptions  
- Achieved 81% accuracy on test set  
- Perfect classification for Lung Cancer (F1 = 1.00); moderate for Thyroid and Colon  

## 📊 Key Results

- BC5CDR outperformed BIONLP13CG in clinical NER tasks  
- Semantic retrieval worked best for well-defined treatment queries  
- DistilBERT showed strong generalization, with optimal performance at Epoch 5  

