# Formula One Radio Natural Language Processing : Emotion, Sentiment & Strategy Intent Detection 🏎️

## Project Overview  
This project applies Natural Language Processing (NLP) techniques to analyze team radio communications from a Formula 1 race. It includes full text preprocessing, exploratory analysis, **radio sentiment and emotion detection using a fine-tuned BERT model**, and **strategic intent classification using TF-IDF vectorization and Logistic Regression**.

The goal is to understand not only the structure of the radio messages, but also the **emotional tone** and **strategic content** conveyed during critical moments of the race.

Beyond analysis, this tool offers **practical utility for the team pit wall**:

- **Strategic Intent Detection** allows teams to be instantly alerted when a rival driver reports an incoming pit stop, tire degradation, or plans for a strategy shift — enabling quick reactions such as preparing an undercut or responding to a threat.

- **Emotion and Sentiment Detection** helps monitor when rival teams raise complaints (e.g., gaining unfair advantage), so teams can take immediate corrective actions like giving a position back to avoid penalties.

By automatically parsing opponent team radios, this tool reduces the cognitive load on race engineers and strategists, helping them focus more on decision-making and less on manually decoding rival communications.


## Features
The project includes the following steps:

1. **Tokenization** – This process breaks down the text into smaller units, such as words or sentences, making it easier to analyze and process further. It helps in understanding the structure of the text and preparing it for subsequent NLP tasks.

2. **Bag of Words (BoW)** – A statistical representation of text where each unique word is counted, disregarding grammar and word order. This technique is useful for feature extraction in text classification and sentiment analysis.

3. **Annotation** – This step involves Part-of-Speech (POS) Tagging, which assigns grammatical categories (e.g., noun, verb) to words, and Named Entity Recognition (NER), which identifies proper names like drivers, teams, and track locations within the transcript.

4. **Normalization** – Techniques such as stemming (reducing words to their root form, e.g., "racing" → "race") and lemmatization (converting words to their base dictionary form, e.g., "driving" → "drive") are applied to standardize text and reduce redundancy.

5. **Word Cloud Representation** – A visual representation of the most frequently occurring words in the dataset, making it easier to identify key terms and themes in the race radio communications.

6. **Stop Word Removal** – Eliminating common, less informative words such as "the," "is," and "and" to improve the efficiency and accuracy of text analysis by focusing on meaningful words.

7. **Radio Sentiment and Emotion Analysis** – A transformer-based model (DistilRoBERTa fine-tuned for emotion classification) is used to detect emotions like joy, anger, and frustration within each radio message. This provides a deeper understanding of driver/team communication tone during the race.

8. **Race Strategy Intent Detection** – A TF-IDF + Logistic Regression pipeline is implemented to classify utterances into strategic intents such as attack, pitting, defending, confirmation, etc. It highlights tactical insights and patterns in race communications.

## Dependencies
Ensure you have the following dependencies installed:
```bash
pip install nltk matplotlib wordcloud pandas seaborn scikit-learn transformers
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
- **HuggingFace Transformers** and a fine-tuned **DistilRoBERTa model** (`j-hartmann/emotion-english-distilroberta-base`) are used for emotion classification of each message.
- **TF-IDF vectorization** combined with **Logistic Regression** is used to train a multi-class classifier for identifying strategic race intents in radio messages. The classification uses a one-vs-rest (OvR) strategy, where a separate binary logistic regression model is trained for each intent class to distinguish it from all other classes. During inference, all models output a probability score, and the class with the highest probability is selected as the predicted intent.

## Author
**Pranit Abraham Thomas**

## License
This project is licensed under the MIT License.

## Note:
The radio communications text used in this project is owned by Formula 1 Group. © 2025 Formula 1 Group. All rights reserved.

```
