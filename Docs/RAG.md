# RAG (Retrieval Augmented Generation)
## What were the problems before RAG?

1. **Hallucinations and Factual Inaccuracy**<br>
One of the most notorious problems was hallucination. Since LLMs are pattern-matching systems, not knowledge databases, they sometimes generate text that is plausible and grammatically correct but factually incorrect or completely fabricated. This happens because the model is trained to predict the next token based on statistical patterns, not to verify information against a source of truth. Without a mechanism to retrieve and verify facts, LLMs could confidently present false information, which was a major roadblock for applications requiring high accuracy, like customer support or legal research.

2. **Stale and Limited Knowledge**<br>
LLMs are trained on massive, static datasets that are often months or even years out of date. This creates a knowledge cutoff, meaning the model has no information about events or data that occurred after its training was completed. For example, a model trained in 2023 would have no knowledge of events from 2024 or 2025. This made them useless for tasks that require current information, such as summarizing recent news or answering questions about a company's most up-to-date policies.

What is RAG (short definition)

RAG (Retrieval-Augmented Generation) = combining a retriever (semantic search over an external knowledge store) with a generator (a language model) so that the LLM’s responses are grounded in real documents.
Simple flow: Query → Retrieve relevant doc chunks → Feed those chunks (context) to the LLM → LLM generates an answer grounded in those chunks.

