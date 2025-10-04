
# Game of Thrones Word2Vec Embeddings

## Overview
This project involves training a **Word2Vec** model on the *Game of Thrones* book series to capture the semantic relationships between characters, locations, and concepts in the story. Using the embeddings, we can explore interesting insights about the relationships between words and characters in the books.

---

## Dataset
- **Source:** *Game of Thrones* book series (all novels)
- **Content:** Text corpus of characters, places, events, and dialogues
- **Preprocessing:** 
  - Lowercasing text  
  - Removing punctuation and special characters  
  - Tokenization  
  - Optional: stopwords removal and lemmatization  

---

## Approach
1. **Text Preprocessing:** Cleaning and tokenizing the text to prepare it for training.
2. **Training Word2Vec:** Using `gensim`’s Word2Vec implementation with parameters tuned for optimal embeddings.
   - **Architecture:** Skip-gram / CBOW (mention which one you used)  
   - **Vector size:** e.g., 100  
   - **Window size:** e.g., 5  
   - **Min count:** e.g., 2  
   - **Epochs:** e.g., 20  
3. **Exploration:** Using trained embeddings to find:
   - Similar characters  
   - Character analogies (e.g., `Jon Snow - Stark + Lannister`)  
   - Semantic clusters of words  

---

## Sample Insights
Here are some interesting observations from the trained Word2Vec model:

- **Most similar characters to `Jon`**: `Arya`, `Robb`, `Sansa`  
- **Analogies**:  
  - `King - Robert + Stannis ≈ Baratheon`  
  - `Winterfell - Stark + Lannister ≈ Casterly Rock`  
- **Clustering**: Characters from the same house or region cluster closely in embedding space  

*Visualizations of embeddings (optional):*  
- t-SNE / PCA plot showing clustering of characters and locations  
- Word similarity heatmaps  

---

## Technologies
- Python  
- [Gensim](https://radimrehurek.com/gensim/models/word2vec.html) for Word2Vec  
- NLTK / SpaCy for preprocessing  
- Matplotlib / Seaborn for visualizations  

---

## How to Run
1. Clone the repository  
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter notebook to see preprocessing, training, and exploration:
   ```bash
   jupyter notebook GoT_Word2Vec.ipynb
   ```

---

## Future Work
- Experiment with **fastText** embeddings for subword information  
- Explore **contextual embeddings** using BERT or GPT models  
- Build a **Game of Thrones character recommendation system** using embeddings  

---

## References
- [Gensim Word2Vec Documentation](https://radimrehurek.com/gensim/models/word2vec.html)  
- [Game of Thrones Wiki](https://awoiaf.westeros.org/index.php/Main_Page)  
