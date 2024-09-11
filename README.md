# Text-Classification-from-Description-using-Context-Similarity-Score

## Hospital Department Recommendation System

This repository contains a system designed to recommend a hospital department based on a description of symptoms provided by the user. The system uses Natural Language Processing (NLP) techniques and machine learning models to find the closest match to the provided symptoms and suggest the most appropriate department.

## Project Overview

The project consists of:

- **Data Preparation**: Preprocessing the dataset to remove duplicates and handle missing values.
- **Feature Extraction**: Using TF-IDF vectorization to convert textual descriptions into numerical data.
- **Model Training**: Calculating cosine similarity between TF-IDF vectors to find the closest match.
- **Model Saving**: Storing the TF-IDF vectorizer and similarity matrix for future use.
- **GUI Interface**: A graphical user interface (GUI) using Tkinter to allow users to input symptom descriptions and receive department recommendations.

## Requirements

To run this project, you'll need:

- Python 3.x
- Required Python libraries (listed below)

You can install the required libraries using pip:

```bash
pip install pandas numpy nltk scikit-learn joblib
```

## Usage

1. **Prepare the Dataset**:
   - Ensure you have a CSV file named `train.csv` with at least two columns: `Desc` (description of symptoms) and `Sub_Department` (the recommended department).
   
2. **Run the Script**:
   - Run the "Desc Pred context.ipynb" in VS Code


## Code Explanation

### Data Preparation

- **Removing Duplicates and Missing Values**:
  The dataset is cleaned to ensure it has unique descriptions and no missing values.

### Feature Extraction

- **TF-IDF Vectorization**:
  TF-IDF (Term Frequency-Inverse Document Frequency) is used to convert the textual data into numerical vectors, which represent the importance of words in the context of the entire dataset.

### Model Training and Saving

- **Cosine Similarity**:
  The cosine similarity metric is used to measure the similarity between the query vector and the dataset vectors.
- **Saving Models**:
  The TF-IDF vectorizer and similarity matrix are saved using `joblib` for later use.

### GUI Interface

- **Tkinter**:
  A simple GUI is created using Tkinter, allowing users to enter symptoms and receive department recommendations. The GUI provides a text entry field for symptoms and a text area to display the results.

## Example

To use the provided example function:

```python
ask_question_using_saved_models("It started subtly, a slight itch at the corner of my nail, barely noticeable. ...")
```

Replace the description with your own symptoms to get a recommendation.

## Notes

- Ensure you have `nltk` data files downloaded for tokenization and lemmatization. You can download them using:

  ```python
  import nltk
  nltk.download('punkt')
  nltk.download('wordnet')
  nltk.download('averaged_perceptron_tagger')
  nltk.download('stopwords')
  ```

- Adjust the dataset path and column names as needed based on your dataset structure.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any questions or feedback, please reach out to [Shukdev Datta] at [shukdevdatta@gmail.com].

```
