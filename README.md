# # RAG With Unsloth Dynamic 4-bit Quantization

## Project Overview

This project implements a Retrieval-Augmented Generation (RAG) pipeline using Unsloth's dynamic 4-bit quantized language model in Google Colab.

The system allows users to upload domain-specific PDF and TXT documents, extract their content, divide the text into smaller chunks, and convert those chunks into numerical embeddings.

FAISS is used as a vector database to retrieve relevant document sections based on user queries. The retrieved information is then provided to a quantized Large Language Model (LLM), which generates context-based responses.

The main goal is to build an efficient document question-answering system while reducing GPU memory consumption through 4-bit model quantization.

## Objectives

- Load an Unsloth dynamic 4-bit quantized language model.
- Upload and process PDF and TXT documents.
- Extract and divide document content into smaller chunks.
- Generate semantic embeddings using Sentence Transformers.
- Store document embeddings in a FAISS vector database.
- Retrieve relevant information based on user queries.
- Generate context-based responses using a quantized LLM.
- Monitor GPU memory usage and optimize resource consumption.

## Technologies Used

- Python
- Google Colab
- Unsloth
- Qwen2.5-1.5B-Instruct (4-bit variant)
- Hugging Face Transformers
- Sentence Transformers
- FAISS
- PyMuPDF
- PyTorch
- NumPy

## Project Workflow

1. **Environment Setup:** Install the required libraries and configure the Google Colab GPU environment.
2. **Model Loading:** Load the Unsloth Qwen 4-bit quantized model.
3. **Document Upload:** Upload PDF or TXT documents.
4. **Text Extraction:** Extract text and document metadata.
5. **Text Chunking:** Divide documents into smaller overlapping chunks.
6. **Embedding Generation:** Convert text chunks into numerical vectors using MiniLM.
7. **Vector Database:** Store embeddings in a FAISS index.
8. **Information Retrieval:** Retrieve relevant document chunks using semantic similarity.
9. **Response Generation:** Provide retrieved context to the quantized LLM to generate answers.
10. **Memory Monitoring:** Monitor GPU memory usage and optimize inference.

## Model and Configuration

| Component | Selection |
|---|---|
| Language Model | Qwen2.5-1.5B-Instruct |
| Model Provider | Unsloth |
| Quantization | Dynamic 4-bit variant |
| Embedding Model | all-MiniLM-L6-v2 |
| Vector Database | FAISS |
| Development Environment | Google Colab |
| Document Formats | PDF and TXT |

## Key Features

- Document-based question answering.
- Semantic search and information retrieval.
- Dynamic 4-bit quantized LLM inference.
- PDF and TXT document processing.
- FAISS-based vector similarity search.
- Context-grounded response generation.
- GPU memory monitoring.
- Interactive question-answering workflow.

## Installation and Requirements

Run the project in Google Colab with GPU acceleration enabled.

Install the required libraries:

```bash
pip install unsloth
pip install sentence-transformers faiss-cpu pymupdf
```

Import the required libraries and load the model using Unsloth's FastLanguageModel interface.

## How to Run

1. Open the project notebook in Google Colab.
2. Select a GPU runtime.
3. Install the required libraries.
4. Import the necessary Python packages.
5. Load the Unsloth 4-bit quantized model.
6. Upload your PDF or TXT documents.
7. Run the document extraction and chunking cells.
8. Generate embeddings and create the FAISS index.
9. Test document retrieval using sample questions.
10. Run the RAG generation function.
11. Ask questions and review the generated responses.
12. Monitor GPU memory consumption.

## Expected Output

The completed system provides:

- Successfully loaded quantized language model.
- Extracted document text.
- Processed text chunks.
- Generated semantic embeddings.
- FAISS vector database.
- Retrieved relevant document sections.
- Context-based answers to user questions.
- GPU memory usage information.

## Memory Optimization

The project uses several techniques to manage GPU resources:

- 4-bit quantized model loading.
- CPU-based embedding generation.
- Limited document retrieval using Top-K search.
- Controlled generation token limits.
- GPU memory monitoring.
- Garbage collection and CUDA cache cleanup.

## Limitations

- Scanned PDFs require OCR for text extraction.
- Retrieval quality depends on document quality and chunking.
- The model may occasionally generate unsupported information.
- GPU memory requirements depend on the selected model and input size.
- The basic FAISS index is stored in the active notebook session and is not automatically persistent.

## Future Improvements

- Develop a Streamlit-based user interface.
- Add OCR support for scanned documents.
- Implement advanced document chunking.
- Add a retrieval reranking mechanism.
- Support additional document formats.
- Improve retrieval accuracy and response evaluation.
- Add persistent vector database storage.

## Learning Outcomes

Through this project, I gained practical experience in:

- Retrieval-Augmented Generation (RAG).
- Large Language Model inference.
- Dynamic 4-bit quantization.
- Semantic embeddings.
- Vector databases and FAISS.
- Document processing and information retrieval.
- GPU memory optimization.
- Building document-based AI applications.

## Conclusion

This project demonstrates the integration of document processing, semantic search, vector databases, and quantized language models in a complete RAG pipeline.

It provides a practical approach to building an efficient document question-answering system using Unsloth and FAISS while considering GPU memory constraints.

## Author

**Name:** [FARYAL]

**Domain:** Generative AI

**Platform:** Google Colab

**Project:** Task 3 – RAG With Unsloth Dynamic 4-bit Quantization
