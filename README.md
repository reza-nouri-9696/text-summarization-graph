# Text Summarization using Sentence Embeddings and PageRank

This Python script performs text summarization using sentence embeddings and the PageRank algorithm. It takes a CSV file containing articles as input and generates summaries for each article.

## Requirements

- Python 3.x
- pandas
- numpy
- nltk
- scikit-learn
- networkx

You can install the required dependencies using pip:

```
pip install pandas numpy nltk scikit-learn networkx
```

Make sure to download the NLTK data by running:

```
python -m nltk.downloader punkt stopwords
```

## Usage

1. Clone this repository or download the script `text_summarization.py`.
2. Place your CSV file containing articles (`tennis_article.csv` in this example) in the same directory.
3. Download the GloVe word embeddings file (`glove.6B.100d.txt`) and place it in the same directory.
4. Run the script:

The script will output the original articles and their corresponding summaries to the console.

## How it works

1. The script reads the articles from the CSV file.
2. It tokenizes the articles into sentences using NLTK's sentence tokenizer.
3. Each sentence is cleaned by removing non-alphabetic characters, converting to lowercase, and removing stopwords.
4. Word embeddings from GloVe are used to represent words in each sentence.
5. Sentence vectors are computed by averaging the word embeddings of words in each sentence.
6. Cosine similarity between sentence vectors is used to construct a similarity matrix.
7. The similarity matrix is converted into a graph, and PageRank is applied to assign importance scores to sentences.
8. Finally, the top-ranked sentences are selected to form the summary.

## Contributing

Contributions are welcome! If you have any suggestions or improvements, feel free to open an issue or create a pull request.

---
