# AI-Medical-Assistant (WIP)
Primary care physicians (PCPs) manage a broad range of patient concerns while working under time pressure, documentation burden, and increasing clinical complexity. The need for quick access to comprehensive, reliable, and source-backed medical knowledge is critical for improving patient outcomes and ensuring informed decision-making in a fast-paced environment.

This project utilizes retrieval-augmented generation (RAG) to parse Merck & Co.'s _Merck Manuals_, the company's medical reference manual that contains over 4,000 pages and 23 sections.

## Business Context
Primary care physicians face increasing pressure from rising patient demand, workforce shortages, documentation burden, EHR inbox overload, and broad clinical complexity. These challenges have accelerated demand for AI medical assistants, with the market estimated around $1.86 billion in 2025 and projected to reach $8.85 billion by 2030. 

While the AI medical assistant market is growing rapidly, the highest-value opportunity is not replacing physician judgment; it is helping PCPs retrieve trusted information faster, reduce cognitive burden, and make existing medical knowledge easier to access. This project focuses specifically on AI-assisted clinical references for primary care physicians.

## Problem Statement
Primary care physicians currently lack a trusted, efficient way to access reliable clinical guidance while managing high patient volume. Without timely access to source-backed medical information, physicians risk spending valuable time and mental energy across several parts of their daily workflow:

* Searching long-form medical reference material
* Synthesizing relevant guidance across broad conditions
* Moving between search, reading, and summarization

If left unaddressed, these workflow pressures can reduce physician capacity, increase burnout risk, and contribute to a projected physician shortage of up to 86,000 by 2036 (AAMC).

## Solution Alignment
Solution development follows the fifth project from UT Austin's Post Graduate Program in Machine Learning & Artificial Intelligence for Business Applications. The program provided a PDF containing Merck & Co's nearly 4,000 page _Merck Manuals_. 

The following steps were completed:

* Selecting a model that balances quality, latency, privacy, and cost
* Establishing a baseline for model responses without prompt engineering or RAG
* Improving model responses with prompt engineering
* Introducing RAG to ensure answers are grounded in Merck Manual content
* Implementing LLM-As-Judge eval to measure groundedness and relevance

## Tradeoffs and Decisions
### Tradeoff #1: Building a RAG vs Claude vs ChatGPT
As LLM capabilities continue to advance, companies must decide how to effectively deploy AI across the enterprise. Three options are emerging:

1. Adopt a Commercial LLM for all use cases (Claude, ChatGPT, Gemini)
* best for experimentation, when companies want to understand "what's possible"
* leverage the harness built by leading AI companies
  
2. Manage all use cases through an open-weight version (Flexible model selection via AWS, Azure, Google Cloud)
* let's companies adjust models based on the complexity of the use cases (many enterprise use cases fall into this bukcet)
  
3. Internally build their entire AI stack (flexible model selection and custom infrastructure)
* Especially valuable when companies are protecting intellectual property 

Open Questions
- How does RAG fit into these choices? I assume number 2?
- When using an open weight version, are companies responsible for the harness?
- How to balance a managed-weight version for simpler cases when an internal build is needed for IP sensitive use cases?
- For enterprises, it's challenging to weigh technical proficiency. Of course companies would love to reduce spend and move to a hybrid or open source approach. How many enterprises have the tech capabilities to do this? if you do it, what about the memory layer? a hybrid approach that incorporates multiple models in the same cloud infrastructure makes sense.
- Are my three options even correct?

#### Tradeoff #2: Choosing a Model Within Project Constraints
UT Austin's course curriculum chose to host this project within Google Collab. This choice made the prototype free to use and easier to run without relying on a commercial LLM. In this context, selecting an open-weight model becomes a key decision point. 

General Notes / Mental model for this tradeoff 
- Commercial models for complex tasks with less data (less mature)
- Open-weight models for tasks with strong datasets, such as customer support (more mature)

Open Questions
- When using google collab, could I select an OpenAI or Anthropic model if desired? or am I confined to open source models or Google's model suite?
- When using an open source model (is this the right term?) with cloud provider infra, what do I need to consider?
- What are reasonable alternatives to the mistral model I selected?

#### Tradeoff #3: Defining a System Prompt Architecture
* defining system prompts, evaluating pass/fail criteria

#### Tradeoff #4: Data Chunking Decisions
* Explain what data chunking is, why I chose this approach
* Embeddings, Vector Databases, Retriever

### Tradeoff #5: Eval criteria for LLM-As-Judge
* Explain what metrics were chosen and why

## What I Learned
* define an architecture for your entire ecosystem
* different models make sense for different use cases / company maturities
* companies must be honest - do they have the budget, patience, and skillsets internally to attempt anything besides a commercial solution?
* Defining when a commercial solution is useful vs managed open-host vs custom build
* Model tradeoffs within selective restraints
