# Flipkart Product Semantic Search with Transformers

This project implements a semantic search system for e-commerce products using pre-trained transformer embeddings.  
The system allows searching Flipkart product descriptions based on the meaning of user queries, not just keyword matching.

## Features

- Uses the Flipkart products dataset from Kaggle.
- Employs the `sentence-transformers` library to generate embeddings.
- Performs semantic similarity search using cosine similarity.
- Returns the top-k most relevant products for any input query.

## Dataset

The dataset used in this project is the [Flipkart products dataset](https://www.kaggle.com/datasets/PromptCloudHQ/flipkart-products) from Kaggle.

## Requirements

- Python 3.7+
- pandas
- sentence-transformers
- torch

You can install the dependencies with:

```bash
pip install pandas sentence-transformers torch

## Usage

1. Load the dataset.  
2. Clean and preprocess product data.  
3. Encode product descriptions using a pre-trained SentenceTransformer model.  
4. Use the `search_products(query, top_k)` function to find products semantically similar to the query.

Example:

```python
search_products("wireless bluetooth headphones", top_k=5)

## Next Steps

- Integrate with a web app using Gradio or Streamlit for an interactive search experience.  
- Fine-tune transformer models using e-commerce data for enhanced accuracy.  
- Expand to multi-modal search, including images and reviews.

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

Made with ❤️ by Özlem
