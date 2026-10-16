# Introduction to Retrieval-Augmented Generation (RAG)

This repository contains an introductory notebook on retrieving relevant text and supplying it as context to a language model. I use it to explain the basic retrieval steps before adding larger frameworks or application-specific logic.

## Overview

Retrieval-augmented generation (RAG) combines a retrieval system with text generation. Given a user query, a retriever selects relevant passages from a collection, and the application can include those passages in the model's context.

A basic pipeline has five parts:

1. **Chunking:** divide source documents into passages.
2. **Embedding:** represent passages as vectors using an embedding model.
3. **Indexing:** store the vectors and associated text or metadata.
4. **Retrieval:** embed the query and find passages using a similarity or distance measure.
5. **Generation:** include retrieved passages in the model input, if a generation step is required.

Chunk size and overlap affect how much context each passage retains. Retrieval quality also depends on the embedding model, the search method, and the source documents.

## Notebook

Start with [RAG proj1.ipynb](RAG%20proj1.ipynb). It explores chunking, embeddings, and similarity-based retrieval.

The notebook is educational material, not a production retrieval service. Its dependencies and data requirements should be checked in the notebook before running it.

## Limitations

Retrieval can provide relevant context, but it does not guarantee correct answers or eliminate hallucinations. Retrieved content can be incomplete, outdated, or misleading. Privacy and security also depend on how data is collected, stored, retrieved, and sent to the model.
