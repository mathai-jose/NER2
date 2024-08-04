# Named Entity Recognition (NER) Comparison using SpaCy and NLTK

This project demonstrates the extraction of named entities (e.g., persons, organizations, locations) from contemporary news articles using both rule-based and machine learning-based approaches. Specifically, it uses NLTK for the rule-based approach and SpaCy for the machine learning-based approach. The project also includes a comparison of the results from both methods.

## Requirements

- Python 3.x
- spaCy
- NLTK
- requests
- An API key from News API

## Setup

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/ner-comparison.git
    cd ner-comparison
    ```

2. Install the required libraries:
    ```sh
    pip install spacy nltk requests
    python -m spacy download en_core_web_sm
    ```

3. Obtain an API key from [News API](https://newsapi.org/) and replace `'your_api_key_here'` in `news_fetcher.py` with your actual API key.

## Usage

1. Fetch a news article and save it to a text file:
    ```sh
    python news_fetcher.py
    ```

2. Extract named entities using NLTK:
    ```sh
    python nltk_ner.py
    ```

3. Extract named entities using SpaCy:
    ```sh
    python spacy_ner.py
    ```

4. Compare the results from NLTK and SpaCy:
    ```sh
    python compare_ner.py
    ```

## Files

- `news_fetcher.py`: Fetches a contemporary news article from News API.
- `nltk_ner.py`: Extracts named entities using NLTK.
- `spacy_ner.py`: Extracts named entities using SpaCy.
- `compare_ner.py`: Compares the named entities extracted by NLTK and SpaCy.
- `README.md`: This readme file.

## Example Output

1. **Entities extracted by NLTK:**
    ```
    [('Apple', 'GPE'), ('U.K.', 'GPE'), ('$1 billion', 'MONEY')]
    ```

2. **Entities extracted by SpaCy:**
    ```
    [('Apple', 'ORG'), ('U.K.', 'GPE'), ('$1 billion', 'MONEY')]
    ```

3. **Comparison of entities extracted by NLTK and SpaCy:**
    ```
    Common Entities:
    [('Apple', 'ORG'), ('U.K.', 'GPE'), ('$1 billion', 'MONEY')]

    Entities only by NLTK:
    []

    Entities only by SpaCy:
    []
    ```

## Observations and Conclusions

- NLTK and SpaCy both successfully extracted similar entities.
- SpaCy provided more specific entity types (e.g., 'ORG' for organizations).
- NLTK's rule-based approach might miss some entities that SpaCy's machine learning model can capture.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any questions or comments, please contact [yourname@yourdomain.com](mailto:yourname@yourdomain.com).

