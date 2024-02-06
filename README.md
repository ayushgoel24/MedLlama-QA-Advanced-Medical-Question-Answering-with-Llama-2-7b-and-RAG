# MedLlama-QA-Advanced-Medical-Question-Answering-with-Llama-2-7b-and-RAG

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![GitHub Issues](https://img.shields.io/github/issues/ayushgoel24/MedLlama-QA-Advanced-Medical-Question-Answering-with-Llama-2-7b-and-RAG.svg)](https://github.com/ayushgoel24/End-to-End-Microservice-Architecture-Scalable-Integrations-and-Performance-Optimizations/issues)
[![Contributions welcome](https://img.shields.io/badge/Contributions-welcome-orange.svg)](https://github.com/ayushgoel24/MedLlama-QA-Advanced-Medical-Question-Answering-with-Llama-2-7b-and-RAG)

Explore MedLlama-QA, a cutting-edge medical question-answering system powered by Llama-2-7b. Leveraging Retrieval Augmented Generation (RAG) and advanced embeddings, this repository delivers precise, contextually accurate answers, reducing hallucinations. With a robust tech stack including MiniLM, Splade, Pinecone, and SageMaker, MedLlama-QA achieves enhanced accuracy and relevance in medical QA, showcasing superior performance in comparison to standard language models.

## Table of Contents
1. [Overview](#overview)
2. [Pipeline](#pipeline)
3. [Key Concepts Used](#key-concepts-used)
4. [Edge Cases](#edge-cases)
5. [Scope of Improvements](#scope-of-improvements)
6. [Dependencies](#dependencies)
7. [Usage](#usage)
8. [Results](#results)

## Overview
The medical field demands precision in question-answering systems, and this repository presents a sophisticated solution leveraging the Llama-2-7b model. Through the Retrieval Augmented Generation (RAG) approach, this system integrates a curated medical knowledge base with Llama-2-7b, ensuring contextually and medically accurate responses. By utilizing embeddings and the computational power of SageMaker and Pinecone, this model addresses the challenges of large language models, promising reduced hallucinations and precise, relevant answers.

## Pipeline

### Data
The 'pubmed' dataset serves as a vast reservoir of medical knowledge. Given the limitations of model window sizes, a chunking strategy breaks down the large text datasets into manageable portions, enabling the model to process and understand contextual information effectively.

### Method

**Embeddings**</br>
- **Dense Embeddings (MiniLM)**: Compact representations of text data, generated from MiniLM, provide fixed-size vectors for every piece of text, ensuring uniformity. These embeddings capture essential information from medical texts, allowing the model to understand and process input data effectively.

- **Sparse Embeddings (Splade)**: Characterized by high-dimensional vectors with mostly zero values, Splade's sparse embeddings capture nuanced relationships in the data. This approach enables the model to capture intricate details in medical texts, enhancing its ability to provide accurate and contextually relevant answers.</br></br>

**Vector Store**</br>
The core of the Retrieval Augmented Generation (RAG) approach lies in the vector store, which plays a crucial role in storing embeddings and facilitating rapid retrievals. Pinecone, chosen for its optimization in managing and querying high-dimensional vectors, is integral to the effectiveness of the RAG approach. Pinecone's efficiency ensures quick similarity searches and enables the model to retrieve semantically related content rapidly.

### Tech Stack
**HuggingFace**: Leveraging the capabilities of the HuggingFace library for managing and fine-tuning language models, this project benefits from a wealth of pre-trained models, including Llama-2-7b.

**Pinecone**: The use of Pinecone as a vector index ensures efficient storage, management, and querying of high-dimensional vectors representing textual data. Its capabilities are pivotal in supporting the RAG approach.

**Sagemaker**: The computational prowess of SageMaker is harnessed for tasks such as embedding generation, retrieval, and overall model development. SageMaker provides a seamless environment for deploying and managing machine learning models at scale.

**Llama2**: The Llama-2 model, developed by Meta AI, forms the foundation of this project. Llama-2-7b, with its large parameter size, serves as the primary generative model for medical question-answering.

## Key Concepts Used
**Retrieval Augmented Generation (RAG)**: This innovative approach combines the inherent knowledge of Llama-2-7b with a curated medical knowledge base. The integration of dense and sparse embeddings, along with Pinecone for efficient retrieval, ensures precise, relevant, and non-hallucinated responses.

## Edge Cases
Considering the extensive nature of medical data, certain edge cases may arise. It is essential to handle queries that fall outside the model's training data to ensure accurate responses. Additionally, the system should be robust enough to handle ambiguous queries and provide meaningful outputs.

## Scope of Improvements
While the current implementation is robust, there is always room for enhancement. Possible improvements include refining the chunking strategy for better contextual understanding and exploring additional embeddings for improved performance. Ongoing research in medical text processing and advancements in language models can be incorporated to further enhance the system's capabilities.

## Dependencies
Ensure the following dependencies are installed:

- HuggingFace
- Pinecone
- Sagemaker
- Llama2

## Usage
Follow these steps to use the system:

Install dependencies.
1. Set up the required environment variables.
2. Run the notebook `MedLlama-QA.ipynb`

## Results
The system exhibits improved accuracy and reduced hallucinations compared to standard language models. Precise and relevant answers are generated through the RAG approach, making it a valuable tool in medical question-answering.

## License
This project is licensed under the MIT License.

## Contact
For any inquiries, please contact me at [ayush.goel2427@gmail.com].

## Acknowledgements
Special thanks to the developers at Meta AI for their contributions to the Llama 2 family of large language models. This project builds upon their work, aiming to contribute to the responsible development of language models in the medical domain.