# NLP Vector Space Semantics: Character Similarity Analysis

## Overview
An information retrieval system that identifies TV show characters based on their dialogue patterns using vector space models and cosine similarity. Built document vectors for six Friends characters and achieved character identification through similarity-based classification.

## Problem Statement
Can we identify which Friends character spoke a line based purely on their linguistic patterns and word usage? This project explores vector space semantics to distinguish between character "voices" using only 300 training lines per character.

## Dataset
- **Source:** Friends TV show scripts (Seasons 1-3)
- **Characters Analyzed:** Monica Geller, Joey Tribbiani, Chandler Bing, Phoebe Buffay, Ross Geller, Rachel Green
- **Training Data:** 300 lines per character (1,800 total)
- **Validation/Test Data:** 30 lines per character
- **Total Corpus:** 53,553 script lines

## Methodology

### 1. Data Preprocessing
- Text tokenization using NLTK
- Stop word removal
- Lemmatization with WordNetLemmatizer
- Advanced NLP with spaCy (en_core_web_md)
- Gender attribution using gender_guesser

### 2. Feature Engineering
- **Bag-of-words representation:** Frequency-based token counting
- **TF-IDF weighting:** Term frequency-inverse document frequency
- **Feature selection:** Identifying distinctive words per character
- **Vector normalization:** L2 normalization for cosine similarity

### 3. Similarity-Based Classification
- **Method:** Cosine similarity between document vectors
- **Approach:** Information retrieval classification
- **Evaluation:** Character identification accuracy on validation and test sets

### 4. Vector Space Transformations
- Explored multiple feature extraction techniques
- Experimented with dimensionality and feature weighting
- Optimized character vector representations for maximal distinction

## Technical Implementation

### Key Features
- Document vectorization pipeline
- Cosine similarity computation
- Character-specific vocabulary analysis
- Multi-stage feature transformation
- Train/validation/test split evaluation

### Libraries & Tools
- **NLP:** NLTK, spaCy (en_core_web_md), TextBlob
- **ML/Math:** NumPy, scikit-learn (DictVectorizer)
- **Data Processing:** Pandas
- **Visualization:** Matplotlib, Seaborn
- **Utilities:** gender_guesser, nlpaug

## Results
- Successfully created distinguishable character vectors
- Demonstrated that linguistic patterns can identify speakers
- Validated approach on held-out test data
- Analyzed which vocabulary features best distinguish characters

## Key Insights
- Characters have distinctive linguistic signatures
- Function words and phrase patterns matter as much as content words
- Limited data (300 lines) is sufficient for character identification
- Vector space models effectively capture stylistic differences

## Project Structure
├── README.md

├── NLP_Vector_Space_Semantics_for_Similarity_between_Friends_Characters.ipynb

└── requirements.txt

## Applications
- Author attribution and forensic linguistics
- Character consistency in screenwriting
- Dialogue generation systems
- Text classification based on writing style
- Chatbot personality modeling

## Future Enhancements
- Extend to all 10 seasons of Friends
- Implement deep learning embeddings (Word2Vec, GloVe, BERT)
- Add sentiment analysis per character
- Build real-time character prediction API
- Compare with neural network classifiers

## Note on Dataset
*Dataset (training.csv, val.csv, test.csv) not included due to size constraints. The notebook demonstrates the complete vector space modeling pipeline including preprocessing, feature extraction, and similarity-based evaluation.*

## Academic Context
This project was completed as part of NLP coursework at Queen Mary University of London, focusing on vector space semantics (Units 8-9).

## Author
Nivesara Tirupati

## References
- Vector space models and information retrieval
- TF-IDF weighting schemes
- Cosine similarity for document comparison
