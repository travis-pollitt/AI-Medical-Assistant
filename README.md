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
<<TBD>>
#### Tradeoff #1: Choosing Between Commercial, Managed Open-Weight, or Self Hosted Open-Weight LLMs
* model economics, inference costs, latency tradeoffs

#### Tradeoff #2: Selecting a Managed Open-Weight Model
* Evaluating open source LLMs for AI medical assistant use case

#### Tradeoff #3: Defining a System Prompt Architecture
* defining system prompts, evaluating pass/fail criteria

#### Tradeoff #4: Data Chunking Decisions
* Explain what data chunking is, why I chose this approach

### Tradeoff #5: Eval criteria for LLM-As-Judge
* Explain what metrics were chosen and why

## What I Learned
<<TBD>>
