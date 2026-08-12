# Langchain PDF Analyser

A LangChain-based question-answering tool for PDF documents, with conversation memory and custom prompt templates.
![License](https://img.shields.io/badge/license-MIT-blue.svg)
## Background

This project started from a [YouTube tutorial](https://www.youtube.com/watch?v=WmuSEfgzcJo&list=LL&index=26&t=7s) on using LangChain for PDF Q&A. The tutorial was built against an older version of the LangChain API, so this implementation updates it for the current API and adds two things the original didn't cover: a conversation memory buffer and configurable prompt templates.

## Features

- Load and index PDF documents for semantic search
- Retrieval-augmented Q&A using ChromaDB as the vector store
- Local inference with Mistral-7B (no external API calls)
- Conversation memory for follow-up questions
- Custom prompt templates for controlling answer style and grounding

## Tech stack

- [LangChain](https://www.langchain.com/) — orchestration
- [ChromaDB](https://www.trychroma.com/) — vector store
- Mistral-7B — local LLM


Once the PDF is indexed, you can ask questions interactively. The memory buffer keeps track of prior turns, so follow-up questions don't need to repeat context.

