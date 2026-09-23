# Sentence Transformer 

##  Project Overview

This project uses a **Sentence Transformer** model to convert sentences into numerical vectors called **embeddings**.

It then uses **Cosine Similarity** to find how similar two sentences are based on their meaning.

##  Objective

* Convert sentences into embeddings.
* Understand the semantic meaning of sentences.
* Calculate similarity between sentences.
* Display sentences having a similarity score greater than `0.5`.

##  Technologies Used

* Python
* Sentence Transformers
* Scikit-learn
* `all-MiniLM-L6-v2`

##  Project Structure

```text
sentense-transformer/
│
├── embedding.py
└── README.md
```

##  Installation

Open the VS Code terminal and install the required libraries:

```bash
pip install sentence-transformers scikit-learn
```

##  Model Used

```text
all-MiniLM-L6-v2
```

This model converts sentences into **384-dimensional embeddings**.

##  How It Works

### 1. Load the Model

```python
model = SentenceTransformer("all-MiniLM-L6-v2")
```

The Sentence Transformer model is loaded.

### 2. Give Input Sentences

Example:

```text
I like apples.
I love eating apples.
I am going to school.
I go to college every day.
```

### 3. Generate Embeddings

```python
embeddings = model.encode(sentences)
```

Each sentence is converted into a numerical vector.

### 4. Calculate Cosine Similarity

```python
similarity = cosine_similarity(embeddings)
```

Cosine similarity measures how similar the meanings of two sentences are.

### 5. Display Similar Sentences

The program displays sentence pairs whose similarity score is greater than `0.5`.

##  How to Run

Open the terminal in the project folder and run:

```bash
python embedding.py
```

##  Sample Output

```text
Total number of sentences: 8
Embedding dimension: 384

--- Embeddings ---

Sentence: I like apples.
Embedding: [...]

Sentence: I love eating apples.
Embedding: [...]

--- Semantic Similarity ---

Sentence 1: I like apples.
Sentence 2: I love eating apples.
Similarity: 0.xxxx
```

##  Key Concepts

### Embedding

An embedding is a numerical representation of a sentence that captures its meaning.

### Sentence Transformer

Sentence Transformer converts sentences into meaningful numerical vectors.

### Cosine Similarity

Cosine Similarity measures the similarity between two vectors.

A score closer to **1** means the sentences are more semantically similar.

##  Result

The project successfully converts sentences into embeddings and identifies semantically similar sentences using **Cosine Similarity**.
