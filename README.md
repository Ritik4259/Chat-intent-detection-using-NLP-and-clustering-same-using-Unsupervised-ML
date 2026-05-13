# Chat Intent Detection using NLP and Clustering using Unsupervised Machine Learning

An end-to-end Natural Language Processing (NLP) project that automatically discovers hidden chat intents from customer conversations using semantic embeddings and unsupervised machine learning techniques.

The project explores and compares multiple text representation approaches including:

* TF-IDF
* Word2Vec
* GloVe
* BERT / Sentence-BERT

along with clustering algorithms such as:

* K-Means
* DBSCAN
* HDBSCAN

to group semantically similar chat messages into meaningful intent clusters without manually labeled data.

---

## Project Objective

The primary objective of this project is to automatically identify and cluster hidden user intents from chat or customer-support conversations.

Instead of manually assigning labels such as:

* Greeting
* Complaint
* Refund Query
* Technical Support

the system learns semantic patterns directly from raw conversations and groups similar messages together using unsupervised learning.

---

## Key Features

* Complete NLP preprocessing pipeline
* Automatic language filtering
* TF-IDF vectorization
* Word2Vec embeddings
* GloVe embeddings
* Sentence-BERT embeddings
* Sentence vector generation
* K-Means clustering
* DBSCAN clustering
* HDBSCAN clustering
* Cluster evaluation metrics
* PCA dimensionality reduction
* t-SNE visualization
* Semantic intent discovery
* Comparative analysis of embedding methods

---

## Technologies Used

### Programming Language

* Python

### Libraries & Frameworks

* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* NLTK
* Gensim
* Sentence-Transformers
* HDBSCAN
* langid
* Regex (`re`)

---

## NLP Pipeline

### 1. Text Preprocessing

The project performs extensive preprocessing on raw chat conversations:

* Lowercasing
* URL removal
* Mention removal
* Punctuation removal
* Number removal
* Extra-space normalization

---

### 2. Tokenization

Implemented tokenization using NLTK's `TweetTokenizer` to properly process social-media-style conversations.

Example:

```python
["payment", "failed", "again"]
```

---

### 3. Stopword Removal

Removed common stopwords while preserving important negation terms such as:

* not
* never
* no

to maintain semantic meaning.

---

### 4. Lemmatization

Reduced words to their root forms.

Examples:

* running → run
* payments → payment
* issues → issue

---

## Embedding Techniques

---

### TF-IDF

Traditional statistical text representation method based on:

* Term Frequency
* Inverse Document Frequency

#### Advantages

* Fast
* Lightweight
* Good baseline approach

---

### Word2Vec

Dense semantic word embedding model developed by Google.

#### Architectures

* CBOW
* Skip-Gram

#### Features

* Captures semantic similarity
* Learns contextual relationships between words

---

### GloVe

Global Vectors for Word Representation developed by Stanford University.

#### Model Used

```python
glove.6B.100d
```

#### Features

* Uses global co-occurrence statistics
* Produces meaningful semantic embeddings

---

### BERT / Sentence-BERT

Transformer-based contextual embeddings for advanced semantic understanding.

#### Advantages

* Context-aware embeddings
* Better semantic clustering
* Improved intent discovery

Example:

* “bank account”
* “river bank”

receive different contextual embeddings.

---

## Clustering Algorithms

---

### K-Means Clustering

Partitions data into K clusters using centroid optimization.

#### Workflow

1. Initialize centroids
2. Assign nearest data points
3. Update centroids
4. Repeat until convergence

---

### DBSCAN

Density-based clustering algorithm.

#### Advantages

* Detects arbitrary cluster shapes
* Handles noise/outliers
* No need to specify cluster count

---

### HDBSCAN

Hierarchical density-based clustering algorithm.

#### Advantages

* Automatic cluster discovery
* Better handling of varying densities
* More robust for semantic embeddings

---

## Evaluation Metrics

### Silhouette Score

Measures cluster separation quality.

Range:

* +1 → excellent clustering
* 0 → overlapping clusters
* negative → poor clustering

---

### Davies-Bouldin Score

Measures cluster compactness and separation.

Lower score indicates better clustering.

---

## Dimensionality Reduction

### PCA (Principal Component Analysis)

Used to reduce high-dimensional embedding vectors before clustering and visualization.

---

### t-SNE Visualization

Used to convert high-dimensional embeddings into 2D representations for cluster visualization.

This helps visualize:

* semantic separation
* cluster overlap
* hidden intent structures

---

## Project Workflow

```text
Raw Chat Data
       ↓
Text Preprocessing
       ↓
Tokenization & Lemmatization
       ↓
Embedding Generation
(TF-IDF / Word2Vec / GloVe / BERT)
       ↓
Sentence Vector Creation
       ↓
Clustering
(KMeans / DBSCAN / HDBSCAN)
       ↓
Cluster Evaluation
       ↓
Visualization
       ↓
Intent Discovery
```

---

## Example Intent Clusters

| Cluster | Intent              |
| ------- | ------------------- |
| 0       | Greetings           |
| 1       | Technical Support   |
| 2       | Customer Complaints |
| 3       | Billing & Delivery  |
| 4       | Refund Queries      |

---

## Repository Structure

```text
├── chat intent word2vec.ipynb
├── chat intent tfidf + kmeans and dbscan.ipynb
├── glove implementation.ipynb
├── bert.ipynb
├── dataset/
├── outputs/
└── README.md
```

---

## Applications

* Customer support analytics
* Chatbot intent discovery
* Ticket categorization
* Feedback analysis
* Conversation mining
* Social media analytics
* Automated support systems

---

## Future Improvements

* BERTopic integration
* UMAP visualization
* Fine-tuned transformer embeddings
* Real-time intent detection API
* Automatic cluster naming
* Web application deployment
* Hybrid embedding approaches

---

## Learning Outcomes

This project helped in understanding:

* NLP preprocessing pipelines
* Semantic embeddings
* Transformer-based NLP
* Unsupervised machine learning
* Clustering algorithms
* Semantic similarity
* Vector representations
* Dimensionality reduction
* Intent mining and discovery

---


[Chat Intent Detection using NLP and Clustering using Unsupervised ML](https://github.com/Ritik4259/Chat-intent-detection-using-NLP-and-clustering-same-using-Unsupervised-ML/tree/main?utm_source=chatgpt.com)
