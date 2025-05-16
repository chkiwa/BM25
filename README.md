# BM25 Resume Search

This project demonstrates how to use the BM25 algorithm to search and rank resumes based on a query. The notebook processes resumes in PDF and DOCX formats, cleans the text, tokenizes it, and applies the BM25 algorithm to retrieve the most relevant resumes.

## Features

- **Resume Parsing**: Extracts text from resumes in `cv_test` folder (supports `.pdf` and `.docx` formats).
- **Text Cleaning**: Removes stopwords, punctuation, and normalizes text to lowercase.
- **BM25 Ranking**: Uses the `rank_bm25` library to rank resumes based on relevance to a query.
- **Query Support**: Supports single-word and multi-word queries.

## Requirements

- Python 3.9 or higher
- Required libraries:
  - `pandas`
  - `fitz` (PyMuPDF)
  - `python-docx`
  - `nltk`
  - `rank_bm25`

## Installation

1. Install the required Python libraries:
   ```bash
   pip install pandas pymupdf python-docx nltk rank_bm25
   ```

2. Download NLTK stopwords:
   ```python
   import nltk
   nltk.download('stopwords')
   ```

## Usage

1. Place resumes in the `cv_test` folder.
2. Open and run the `bm25.ipynb` notebook to:
   - Parse and clean the resumes.
   - Tokenize the text.
   - Apply the BM25 algorithm.
3. Input a query to retrieve the top 5 most relevant resumes.

### Example Query

```python
query = "Openshift Kubernetes System Linux Automatisation"
```

The notebook will output the filenames of the top 5 resumes matching the query.

### Notes

- Ensure the `cv_test` folder contains resumes before running the notebook.
- The BM25 algorithm is case-insensitive and works best with preprocessed text.

## License

This project is for educational purposes and does not include a specific license. You are free to use and modify the code for personal or academic use.