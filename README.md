# Fine-tuned Retrieval-Augmented Generation (RAG) Chatbot

## Overview
This project focuses on enhancing a movie recommendation chatbot using the Retrieval-Augmented Generation (RAG) methodology. The chatbot leverages a vector store database, Pinecone, for efficient information retrieval and employs the Langchain framework for the RAG pipeline. Additionally, the Llama-2-7b model serves as the backbone, fine-tuned to optimize performance.

## Techniques and Components
### 1. Vector Store Database
- Utilizes Pinecone for optimized ranking in small to medium-sized datasets (≤100k records).
- Incorporates movie embeddings, generated using the Llama-2-7b model, along with metadata, actors' names, and genres.

### 2. RAG Pipeline Framework
- Implements Langchain for the RAG pipeline, offering low-level configurability.
- Fine-tunes Llama-2-7b using 4-bit precision through QLoRA for efficient memory usage and adaptation to movie recommendation tasks.

### 3. Prompting Strategies
- Tailors the RAG pipeline prompt for movie recommendations.
- Emphasizes limitations and goals, instructing the chatbot to focus on user preferences and not provide information beyond the vector store context.

### 4. Models Evaluation
- Utilizes Average Embedding Cosine Similarity and Relevance Accuracy metrics for comprehensive model assessment.
- Compares base Llama-2-7b-chat with RAG-based Llama-2-7b-chat, fine-tuned versions, and various prompting techniques.

### 5. Streamlit Chatbot Interface
- Creates an immersive interface using Streamlit for users to interact with the movie recommendation chatbot seamlessly.

## Performance Comparisons
### 1. Base vs. RAG-Based Models
- RAG-based model outperforms the base model by a 4% difference in mean embedding cosine similarity and recommends 19/20 relevant movies compared to 14/20 for the base model.

### 2. Fine-tuned vs. RAG-Based Fine-tuned Models
- RAG-based fine-tuned model shows an 8% improvement in mean embedding cosine similarity compared to the fine-tuned base model, with equal relevance accuracy.

### 3. RAG-Based Models with Varying k Values
- Performance remains consistent for both RAG-based models across different k values (3, 4, 5), maximizing at k=4 for both mean cosine similarity and relevance accuracy.

### 4. Prompting Techniques
- Different prompting techniques show varying effects on performance, emphasizing the importance of tailoring prompts for specific contexts.

## Limitations and Future Work
- Limited computing resources constrained the extent of experimentation and model evaluation.
- Future work involves exploring the impact of different embedding models on context retrieval quality and experimenting with novel AI models beyond Llama-2-7b
