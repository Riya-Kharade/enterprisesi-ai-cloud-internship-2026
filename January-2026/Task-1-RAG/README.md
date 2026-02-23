# Task 1: Combining Company Knowledge with AI using RAG

## Intern Details

-   Name: Riya Sunil Kharade
-   Internship Role: AI & Cloud Research Intern

------------------------------------------------------------------------

## Reference

YouTube Session: Combining Company Knowledge with AI using
Retrieval-Augmented Generation (RAG)\
Link: https://youtu.be/ERQCq1RUTQc

------------------------------------------------------------------------

## 1. Introduction

Large Language Models (LLMs) such as ChatGPT are powerful tools trained
on public data. However, they do not have access to internal company
knowledge, which is essential for enterprise use cases.

Retrieval-Augmented Generation (RAG) solves this problem by combining
company data with AI models at query time. This task explains how RAG
works, its challenges, and advanced approaches.

------------------------------------------------------------------------

## 2. Importance of Company Knowledge

LLMs have limitations such as:

-   Training only on public data\
-   Knowledge cutoff\
-   Hallucinated responses\
-   Lack of traceability

For business use, AI systems must:

-   Use domain-specific knowledge\
-   Access real-time internal data\
-   Provide trustworthy answers

RAG enables this without retraining models.

------------------------------------------------------------------------

## 3. Challenges with Large Context Windows

Using large context windows leads to:

-   High cost\
-   Slow response time\
-   Information overload\
-   "Needle in a haystack" problem

Solution: Provide only relevant information using retrieval systems.

------------------------------------------------------------------------

## 4. Why LLMs Cannot Access Internal Knowledge

LLMs generate responses based on training data only. They cannot:

-   Access private databases\
-   Retrieve real-time data\
-   Provide source references

This limits enterprise reliability.

------------------------------------------------------------------------

## 5. What is Retrieval-Augmented Generation (RAG)

RAG has two main components:

### Indexing (Ingestion)

-   Prepare company data\
-   Convert to embeddings\
-   Store in vector database

### Retrieval (Inference)

-   Retrieve relevant data\
-   Add to prompt\
-   Generate grounded response

Vector databases enable semantic search.

------------------------------------------------------------------------

## 6. Naïve RAG Example (Recipe Use Case)

Example workflow:

-   Recipes stored and embedded\
-   Data chunked\
-   Relevant chunks retrieved

Problems observed:

-   Mixed instructions\
-   Loss of context\
-   Incorrect answers

------------------------------------------------------------------------

## 7. Key Challenges in Naïve RAG

### 7.1 Poor Indexing

-   Context loss\
-   Mixed documents

Solution: - Larger chunks\
- Metadata tagging

### 7.2 Hallucination

-   Confident wrong answers

Solution: - Guardrails\
- Strict prompts\
- Response blocking

### 7.3 Structured Data Issues

-   Semantic search fails on numbers

Solution: - Metadata filtering\
- Structured extraction

------------------------------------------------------------------------

## 8. High-Level RAG Architecture

RAG consists of:

-   Indexing pipeline\
-   Retrieval system\
-   Prompt enrichment\
-   LLM response generation

This ensures grounded outputs.

------------------------------------------------------------------------

## 9. Advanced RAG with AI-assisted Indexing

AI improves indexing by:

-   Extracting metadata\
-   Normalizing data\
-   Summarizing documents\
-   Enriching context

This improves retrieval quality.

------------------------------------------------------------------------

## 10. Agentic RAG Architecture

Agentic RAG enables:

-   Tool selection\
-   Iterative retrieval\
-   Query rewriting\
-   Multi-source access

Tools include:

-   Vector search\
-   SQL queries\
-   Knowledge graphs\
-   APIs

------------------------------------------------------------------------

## 11. AI Evaluation

LLMs are:

-   Non-deterministic\
-   Sensitive to prompts\
-   Frequently updated

Evaluation Process:

-   Prepare test dataset\
-   Generate responses\
-   Compare outputs\
-   Calculate metrics

Metrics include:

-   Correctness\
-   Groundedness\
-   Relevance\
-   Helpfulness

------------------------------------------------------------------------

## 12. Vector Database Working

### Step 1: Input Data

Text, images, videos, and audio

### Step 2: Embedding Model

Converts data into vectors

### Step 3: Vector Embeddings

Numeric representations of meaning

### Step 4: Storage

Stored in vector database for search

------------------------------------------------------------------------

## 13. Evaluation Pipeline in n8n

Steps:

1.  Input evaluation dataset\
2.  Execute AI agent\
3.  Store outputs\
4.  LLM-based evaluation\
5.  Metric calculation\
6.  Visualization

This ensures continuous quality monitoring.

------------------------------------------------------------------------

## 14. Importance of Evaluation

-   Models change over time\
-   Manual testing is not scalable\
-   Automation ensures consistency

Evaluation is critical for enterprise AI.

------------------------------------------------------------------------

## 15. Key Takeaways

-   Data preparation is business logic\
-   Strong indexing is essential\
-   Agentic RAG is emerging\
-   Evaluation is mandatory\
-   Automation ensures quality

------------------------------------------------------------------------

## Conclusion

Retrieval-Augmented Generation enables AI systems to use company
knowledge effectively.

By improving indexing, using metadata, adopting agent-based
architectures, and implementing automated evaluation, organizations can
build scalable, trustworthy, and enterprise-ready AI applications.
