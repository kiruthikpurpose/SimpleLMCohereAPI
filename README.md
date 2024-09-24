
## Simple Language Model Using Cohere API

This project demonstrates the use of the Cohere API to build a simple language model capable of answering questions based on a provided text. The notebook includes examples of various queries related to Indian beaches and uses the Cohere API to generate responses.

### Requirements

- Cohere API key (get it from [cohere.com](https://cohere.com))
- Python libraries: `cohere`, `numpy`, `pandas`, `annoy`, `warnings`

### Features

- Embedding text data using Cohere's language model.
- Creating a search index with `Annoy` to find similar text based on user queries.
- Generating responses to user queries using Cohere's `generate` function.

### How to Use

1. **Install the Required Libraries:**

   ```python
   !pip install cohere numpy pandas annoy
   ```

2. **Set Up the Cohere API Key:**

   Replace the placeholder `<Get your Cohere API Key from cohere.com>` in the code with your actual API key.

   ```python
   co = cohere.Client('<Your API Key>')
   ```

3. **Running the Code:**

   Execute the notebook in Google Colab for faster execution using GPU or TPU. Simply run all cells in order to initialize the Cohere client, generate embeddings, create a search index, and then run queries.

4. **Examples of Queries:**

   The notebook contains pre-defined questions like:

   - "Which Indian beach should I visit?"
   - "Which Indian beach is family-friendly?"
   - "Which Indian beach has a lighthouse?"

   You can modify these or add your own queries.

### Code Structure

- **Importing Libraries:** Import required libraries such as `cohere`, `numpy`, `pandas`, `annoy`, and `warnings`.
- **Defining Question and Text Data:** Sample question and text data about Indian beaches.
- **Data Preparation:** Split the text data into paragraphs and clean them.
- **Generating Embeddings:** Use Cohere's `embed` function to get embeddings for the text data.
- **Creating Search Index:** Use `Annoy` to create a search index for the embeddings.
- **Searching for Similar Text:** Define a function `search_text(query)` to retrieve text segments similar to the query.
- **Generating Answers:** Define a function `ask_llm(question)` to generate answers using Cohere's `generate` function.

### Google Colab Link

Click the badge below to open the notebook in Google Colab:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kiruthikpurpose/SimpleLMCohereAPI/blob/main/SimpleLanguageModelUsingCohere.ipynb)

### License

This project is licensed under the MIT License - see the LICENSE file for details.
