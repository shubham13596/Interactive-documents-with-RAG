# Interactive Long Document Chat Interface

## Objective

This project aims to transform the experience of interacting with long documents by converting them into a more engaging chat-based interface. Utilizing the power of retrieval-augmented generation with Langchain, users can interact with long documents in a conversational manner, making the reading process more dynamic and interesting.

**Use-cases**: Interactive documentation alone will not build trust. What builds trust is showing the user the source within the document from where the answer has been generated (similar to how Google shows references/citations to enhance trust). Interfaces like these can make a world of difference in cases where trust is in deficit. I have explained the example of how loan documentation/terms and conditions can be made interactive to improve trust in the loan disbursal process for the customer. The Medium link is here: [Making Dreaded T&Cs Easy with LLMS](https://medium.com/@shubham13596/making-dreaded-tncs-easy-with-llms-fd2e35d7fe92).

## How It Works

The system operates through the following steps:

1. **Upload PDF File**: Users begin by uploading the PDF file of the long document they wish to interact with.
2. **Document Splitting**: The uploaded document is then split into manageable chunks for easier processing.
3. **Embedding Creation**: Each chunk of the document is processed to create embeddings, which are essentially numerical representations capturing the essence of the text.
4. **VectorStore**: These embeddings are stored in a VectorStore, an efficient storage mechanism that facilitates quick retrieval.
5. **Interaction Through Questions**: Users interact with the system by asking questions.
6. **Question Embedding**: Each user question is converted into an embedding using OpenAI's advanced language models.
7. **Semantic Similarity Matching**: The system then computes the semantic similarity between the question embedding and the document chunk embeddings.
8. **Retrieval and Response Generation**: The chunk with the highest similarity score is passed to a large language model (LLM) to generate a user-friendly answer, creating a chat-like experience.
9. **Chat interface**: Gradio is used as a chat interface for demo purposes

## Features

- **User-Friendly Interface**: Easy to use interface for uploading documents and interacting with the system.
- **Advanced NLP Techniques**: Utilizes cutting-edge natural language processing techniques for accurate semantic matching.
- **Scalable and Efficient**: Designed to handle long documents efficiently.

## Technologies Used

- Langchain
- Gradio
- OpenAI APIs
- VectorStore Implementation
