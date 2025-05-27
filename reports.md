# Flipkart Product Semantic Search - Project Report

## 1. Project Objective & Problem Definition

**What are we doing?**  
We are building a semantic search system over the Flipkart products dataset, which matches user queries in natural language to product descriptions based on meaning, not just keywords.

**Why?**  
To provide more relevant product recommendations beyond simple keyword matching, improving user experience and potentially increasing sales conversions.

---

## 2. Dataset

**What did we use?**  
The Flipkart product dataset from Kaggle, containing product names, descriptions, prices, and more.

**How did we process it?**  
- Loaded the dataset using Pandas.  
- Cleaned missing or irrelevant entries (e.g., empty descriptions).  
- Selected relevant columns for the task.

**Outcome**  
A clean, manageable list of product descriptions ready for processing.

---

## 3. Data Preprocessing

**What did we do?**  
Cleaned text by removing unwanted characters, HTML tags, and normalized case.

**Why?**  
To help the model better understand and consistently process the input data.

**How?**  
- Converted text to lowercase.  
- Removed punctuation and extra whitespace.

**Outcome**  
Consistent and clean text data ready for embedding generation.

---

## 4. Embedding Generation

**What did we do?**  
Used a pre-trained transformer model from the `sentence-transformers` library.

**Why?**  
Transformers capture contextual meaning, allowing us to convert product descriptions into meaningful numerical vectors.

**How?**  
- Loaded a pre-trained model (e.g., `all-MiniLM-L6-v2`).  
- Generated embeddings for each product description.  
- Stored embeddings for later similarity computations.

**Outcome**  
Numerical vector representations for each product capturing semantic information.

---

## 5. Search Functionality

**What did we do?**  
Converted user queries into embeddings to compare with product embeddings.

**Why?**  
We need to represent queries in the same vector space to find semantically similar products.

**How?**  
- Embedded the user’s natural language query.  
- Calculated cosine similarity between query and product embeddings.  
- Retrieved and returned top-k most similar products.

**Outcome**  
Relevant products retrieved based on semantic similarity to the query.

---

## 6. Results & Evaluation

**What did we observe?**  
- Semantic search effectively retrieves relevant products even without exact keyword matches.  
- For example, the query “wireless headphones” returns related products like Bluetooth headphones.

**What can be improved?**  
- Using larger or domain-specific transformer models for better accuracy.  
- Enhancing query preprocessing.  
- Incorporating additional product metadata like images or prices for richer results.

---

## 7. Next Steps

- Build an interactive web app using Gradio or Streamlit.  
- Improve user query handling and preprocessing.  
- Add multi-lingual support.  
- Fine-tune transformer models on domain-specific data.

---

Made with ❤️ by Özlem
