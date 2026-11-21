# azure-rag-job-posting-assistant
Document-grounded AI assistant built with Microsoft Foundry to answer job posting questions using RAG.


# Azure RAG Job Posting Assistant

An AI-powered assistant built using Microsoft Foundry that answers questions about job postings using Retrieval-Augmented Generation (RAG).

## Project Overview

Job descriptions often contain extensive technical requirements, qualifications, and employment details. This project explores how RAG can help users extract relevant information from a job posting while reducing unsupported or fabricated responses.

The assistant was developed and tested using a Citi Junior Generative AI Application Developer job posting.

## Technologies Used

- Microsoft Foundry (Azure AI)
- GPT-5.4-mini
- text-embedding-3-small
- Retrieval-Augmented Generation (RAG)
- Document indexing and retrieval
- Prompt engineering
- AI evaluation and observability

## How It Works

1. A PDF job posting is uploaded and indexed in Microsoft Foundry.
2. A user submits a question about the position.
3. The agent retrieves relevant passages from the indexed document.
4. GPT-5.4-mini generates an answer grounded in the retrieved information.
5. Agent instructions require the assistant to avoid unsupported claims and acknowledge information missing from the posting.

## Evaluation Results

The agent was evaluated using 15 questions covering job requirements, technologies, employment details, and information not explicitly stated in the document.

| Evaluation Metric | Result |
|---|---|
| Response Completeness | 100% (15/15) |
| Relevance | 100% (15/15) |
| Similarity | 100% (15/15) |
| Tool Output Utilization | 93% (14/15) |

The retrieval-quality evaluator could not produce a score because of an input-format error. Retrieval activity was separately verified through agent traces.

One tool-output-utilization test was flagged for a potentially unsupported statement, highlighting the importance of checking grounding beyond overall response quality.

## Key Learnings

- Building document-grounded AI agents using Microsoft Foundry
- Understanding retrieval and LLM-generated responses
- Designing prompts to handle missing information and misleading questions
- Using evaluation metrics and traces to investigate model behavior
- Identifying limitations in automated AI evaluation

## Future Improvements

- Support multiple job postings
- Improve retrieval-quality evaluation
- Expand testing across different job descriptions
- Explore a user-facing interface
