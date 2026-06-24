# AI-Medical-Assistant
The healthcare industry is rapidly evolving, with primary care physicians facing increasing challenges in managing vast volumes of medical data while delivering accurate and timely diagnoses. The need for quick access to comprehensive, reliable, and up-to-date medical knowledge is critical for improving patient outcomes and ensuring informed decision-making in a fast-paced environment.

This project utilizes retrieval-augmented generation (RAG) to parse Merck & Co.'s "Merck Manuals", the company's medical reference manual that contains over 4,000 pages and 23 sections.

## Business Context
Primary care physicians face increasing pressure from rising patient demand, workforce shortages, documentation burden, EHR inbox overload, and broad clinical complexity. These challenges fuel an AI medical assistant market that was estimated around $1.86 billion in 2025 and projects to reach $8.85 billion by 2030. 

While the AI medical assistant market is growing rapidly, the highest-value opportunity is not replacing physician judgment; it is helping PCPs retrieve reliable clinical guidance, reduce cognitive burden, and complete routine documentation and follow-up work more efficiently.

## Problem Statement
Primary care physicians currently lack a trusted, efficient way to access reliable clinical guidance while managing high patient volume, broad clinical complexity, documentation demands, and EHR inbox overload. Without timely access to source-backed medical information, physicians risk spending valuable time and mental energy across several parts of their daily workflow:

* Searching for relevant clinical guidance when advising patients
* Managing heavy cognitive load across broad and complex patient concerns
* Completing after-hours documentation, inbox triage, and follow-up work

If left unaddressed, these workflow pressures can reduce physician capacity, increase burnout risk, and contribute to a projected physician shortage of up to 86,000 by 2036 (AAMC).

## Solution Alignment
Solution development follows the fifth project from UT Austin's Post Graduate Program in Machine Learning & Artificial Intelligence for Business Applications. The program provided a portable document format (PDF) containing Merck & Co's nearly 4,000 page medical manual. The following steps were completed to create a medical assistant that parses Merck Manuals.

* Model Selection: Selecting an open source LLM model
* Medical question answering using LLM
* Medical question answering using LLM and prompt engineering
* Medical question answering using LLM, prompt engineering, and retrieval-augmented generation
* Deployed LLM-As-Judge eval to measure groundedness and relevance

## Tradeoffs and Decisions
<<TBD>>

## What I Learned
<<TBD>>
