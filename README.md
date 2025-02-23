# Generative Search Help Mate AI

Your AI-Powered Intelligent Search Assistant for Insurance Documents

## Table of Contents
- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Approach](#approach)
- [Features](#features)
- [Technologies/Libraries Used](#technologieslibraries-used)
- [Installation](#installation)
- [Usage](#usage)
- [Demonstration](#demonstration)
- [Conclusions](#conclusions)
- [Glossary](#glossary)
- [Acknowledgements](#acknowledgements)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## Introduction
Generative Search Help Mate AI is a system designed to perform intelligent document searches using semantic search and re-ranking techniques. It processes PDF documents, retrieves relevant information, and generates responses based on the search results.

## Problem Statement
Traditional keyword-based searches often fail to retrieve accurate information from complex insurance policy documents due to ambiguous terms and lack of contextual understanding.

This project aims to build a Retrieval-Augmented Generation (RAG) based generative search system that enhances search accuracy by:

- Using efficient text chunking for better document processing.
- Leveraging semantic search and re-ranking for relevant results.
- Generating context-aware answers using a robust AI model.

This system will provide precise, efficient, and user-friendly access to policy information, overcoming the limitations of conventional search methods.

## Objectives
- To develop an AI-powered search system that retrieves contextually relevant information.
- To integrate semantic search and re-ranking techniques for better search results.
- To provide an efficient and user-friendly document search experience.

## Approach
- Extract and preprocess text from PDF documents.
- Generate embeddings for document chunks using transformer-based models.
- Perform semantic search with caching for efficiency.
- Re-rank search results to improve relevance.
- Generate responses based on retrieved information.

## Features
- **Semantic Search**: Retrieves contextually relevant document excerpts.
- **Re-ranking**: Enhances search result relevance using AI-based ranking models.
- **Efficient Caching**: Stores frequently searched results for faster retrieval.
- **Automated Response Generation**: Provides summarized answers based on search results.

## Technologies/Libraries Used
- Python 3.11 or higher
- pdfplumber
- tiktoken
- OpenAI API
- ChromaDB
- Sentence-Transformers

## Installation
### Prerequisites
- Python 3.11 or higher
- pip (Python package installer)

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/Generative-Search-Help-Mate-AI.git
   cd Generative-Search-Help-Mate-AI
   ```
2. Create a virtual environment:
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
3. Install the required packages:
   ```sh
   pip install -r requirements.txt
   ```
4. Set up environment variables:
   - Create a `.env` file in the root directory.
   - Add your OpenAI API key:
     ```sh
     OPENAI_API_KEY=your_openai_api_key
     ```


## Usage
### 1. Install and Import the Required Libraries
The notebook installs and imports the necessary libraries such as `pdfplumber`, `tiktoken`, `openai`, `chromadb`, and `sentence-transformers`.

### 2. Read, Process, and Chunk the PDF Files
The project uses `pdfplumber` to read and process PDF files. The path to the PDF file is defined, and the file is read and chunked for further processing.

### 3. Semantic Search with Cache
The project performs a semantic search of a query in the collection embeddings to retrieve the top semantically similar results. The search results are cached for efficiency.

### 4. Re-rank Scores
The top search results are re-ranked based on their relevance to the input query.

### 5. Generative Search
The project generates responses based on the top re-ranked search results.

### 6. Evaluate Sample Queries
Sample queries are evaluated to demonstrate the functionality of the generative search system.

## Functions

### `semantic_search(input_query)`
Performs a semantic search for the given input query and returns the search results.

### `rerank_scores(input_query, search_df)`
Re-ranks the search results based on their relevance to the input query.

### `search_results_RAG(input_query)`
Combines semantic search and re-ranking to generate the final response for the input query.

### `generative_search(query, top_3_RAG)`
Generate a response using GPT-3.5's ChatCompletion based on the user query and retrieved information.

## Demonstration
You can view the [demo materials](https://github.com/arnabberawork/Help-Mate-AI/tree/main/Demo)

## Conclusions
Generative Search Help Mate AI enhances document search accuracy by utilizing semantic search and re-ranking techniques. This project enables efficient retrieval of relevant information from large document repositories.

## Glossary
- **Semantic Search**: AI-based search method that considers contextual meaning rather than just keywords.
- **Re-ranking**: A technique to improve search result relevance using AI-based ranking models.
- **ChromaDB**: A database optimized for embedding-based search.
- **Transformer Models**: Advanced deep learning models used for NLP tasks.

## Acknowledgements
- The project references presentations in upGrad’s recorded module given by [Aditya Bhattacharya](https://www.linkedin.com/in/aditya-bhattacharya-b59155b6/).
- The project references presentations in upGrad’s recorded module given by [Akshay Ginodia](https://www.linkedin.com/in/akshay-ginodia-6a7094a3/).
- The project references insights and inferences from presentations in upGrad’s doubt clear session given by [Shridhar Galande](https://www.linkedin.com/in/shridhar-galande/).
- The project references presentations in upGrad's live class given by [Sheshanth AS](https://www.linkedin.com/in/sheshanthas/).

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request for improvements or bug fixes.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Author
* [Arnab Bera](https://www.linkedin.com/in/arnabbera-tech/)
