# Retrieval-Augmented Generation (RAG)

---
## Content
   - [What is RAG?](#what-is-rag)
   - Basic RAG
   - Advanced RAG

---
### What is RAG?
Retrieval-augmented generation is a technique used in natural language processing that combines the power of both retrieval-based models and generative models to enhance the quality and relevance of generated text.

Retrieval-augmented generation has 2 main componenets:
   - **Retrieval models:** These models are designed to retrieve relevant information from a given set of documents or a knowledge base. (for further details check Information Retrieval Lecture from Stanford [here](https://web.stanford.edu/class/cs224u/slides/cs224u-neuralir-2023-handout.pdf))
   - **Generative models:** Generative models, on the other hand, are designed to generate new content based on a given prompt or context.

Retrieval-augmented generation combines these two approaches to overcome their individual limitations. 
In this framework, a retrieval-based model is used to retrieve relevant information from a knowledge base or a set of documents based on a given query or context. 
The retrieved information is then used as input or additional context for the generative model. 
The generative model can leverage the accuracy and specificity of the retrieval-based model to produce more relevant and accurate text. 
It helps the generative model to stay grounded in the available knowledge and generate text that aligns with the retrieved information. 

---
### Basic RAG
<kbd>   
 <img width="700" src="https://gradientflow.com/wp-content/uploads/2023/10/newsletter87-RAG-simple.png">
</kbd>   

#### The technical implementation of RAG 
- Data preparation:
   1. **Source data:** This data serves as the knowledge reservoir that the retrieval model scans through to find relevant information.
   2. **Data chunking:** Data is divided into manageable “chunks” or segments. This chunking process ensures that the system can efficiently scan through the data and enables quick retrieval of relevant content.
   3. **Text-to-vector conversion (Embeddings):** Converting the textual data into a format that the model can readily use. When using a vector database, this means transforming the text into mathematical vectors via a process known as “embedding.”
   4. **Links between source data and embeddings:** The link between the source data and embeddings is the linchpin of the RAG architecture. A well-orchestrated match between them ensures that the retrieval model fetches the most relevant information, which in turn informs the generative model to produce meaningful and accurate text.

- Retrieval augmented generation
   1. **User query:** The user inputs a query asking for something.
   2. **Embedding:** convert the user query to embedding for better search.
   3. **Search-index:** Search for relevant context to the user query input in the index.
   4. **Generation:** Feed both user query input and retrieved context to LLM to generate an answer.
 
---
### Advanced RAG




















