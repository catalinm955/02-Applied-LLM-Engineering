# Overview
## Step 1 — Dataset (realistic, 50–100 sentences)
- Use a generated realistic corpus:
  - Mixed technical / semi-technical text
  - Enough semantic overlap to test similarity
  - Stored as a .txt or .json
    
This mirrors real RAG ingestion later.

## Step 2 — Token → Sentence embeddings (important!)
- Load a transformer model
- Extract token embeddings
- Apply mean pooling manually
- Compare with SentenceTransformer.encode()

## Step 3 — Similarity metrics (hands-on)
- Compute cosine similarity by hand for 2 vectors
- Compute it with NumPy
- Compare normalized vs non-normalized vectors
- Observe ranking differences

## Step 4 — Mini-exercise (checkpoint)
- Why cosine similarity is preferred over Euclidean in high-D spaces
- What breaks if vectors aren’t normalized
- How pooling choice affects retrieval quality
