Mean pooling
When we do a semantic search via cosine_similarity for example, the model will perform a mean pooling between the sentences. For example:
- Sentence 1 = ["I learn AI"]
- Sentence 2 = ["AI is my favorite topic"]

Sentence 1 has 3 tokens, while sentence 2 has 5 tokens, then the model computes the mean pooling for each one:
mean_pooling_1 = average of all embeddings in the sentence <br>
<img width="237" height="77" alt="image" src="https://github.com/user-attachments/assets/8b6d6f13-ea09-4f9c-b1cd-a6a2129ae793" />


Padding <br>
Since Transformers require sentences of the same length, padding is the operation of setting all the sentences on the same length, by adding "dummy tokens", usually zeros. <br>
These dummy tokens needs to be ignored when we mean pooling and this is when attention-mask come into play by setting all dummy tokens to 0 and 1 for real ones.

