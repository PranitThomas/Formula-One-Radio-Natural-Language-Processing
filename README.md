# Formula One Radio Natural Language Processing 🏎️

## Project Overview
This project applies Natural Language Processing (NLP) techniques to analyze a corpus extracted from a Formula 1 race radio transcript. The goal is to preprocess, analyze, and visualize the textual data using various NLP methodologies.

## Features
The project includes the following steps:

1. **Tokenization** – This process breaks down the text into smaller units, such as words or sentences, making it easier to analyze and process further. It helps in understanding the structure of the text and preparing it for subsequent NLP tasks.

2. **Bag of Words (BoW)** – A statistical representation of text where each unique word is counted, disregarding grammar and word order. This technique is useful for feature extraction in text classification and sentiment analysis.

3. **Annotation** – This step involves Part-of-Speech (POS) Tagging, which assigns grammatical categories (e.g., noun, verb) to words, and Named Entity Recognition (NER), which identifies proper names like drivers, teams, and track locations within the transcript.

4. **Normalization** – Techniques such as stemming (reducing words to their root form, e.g., "racing" → "race") and lemmatization (converting words to their base dictionary form, e.g., "driving" → "drive") are applied to standardize text and reduce redundancy.

5. **Word Cloud Representation** – A visual representation of the most frequently occurring words in the dataset, making it easier to identify key terms and themes in the race radio communications.

6. **Stop Word Removal** – Eliminating common, less informative words such as "the," "is," and "and" to improve the efficiency and accuracy of text analysis by focusing on meaningful words.

## Dependencies
Ensure you have the following dependencies installed:
```bash
pip install nltk matplotlib wordcloud pandas seaborn
```

## Setup & Usage
1. Clone this repository:
   ```bash
   git clone https://github.com/PranitThomas/Formula-One-Radio-Natural-Language-Processing.git
   cd Formula-One-Radio-Natural-Language-Processing
   ```
2. Open the Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Run the notebook to execute all NLP processing steps.

## Implementation Details
- The F1 race radio transcript is stored as text and preprocessed using NLP techniques.
- **NLTK** is used for tokenization, POS tagging, NER, stemming, and lemmatization.
- **WordCloud** is used to generate a visualization of frequent words.
- The processed data is structured and displayed in tabular format.

## Author
**Pranit Abraham Thomas**

## License
This project is licensed under the MIT License.

