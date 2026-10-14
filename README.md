# Awesome-Retrieval-Augmented-Generation-Diagnostics

# Top Retrieval-Augmented Generation Diagnostics Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Hallucination Detection, Context Retrieval Quality & LLM Evaluation Pipelines*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Retrieval-Augmented Generation (RAG) Diagnostics**. These tools evaluate RAG pipelines end-to-end — measuring faithfulness, context relevance, answer correctness, and hallucination vectors — so teams can catch regressions, diagnose retrieval failures, and ship reliable AI applications.

**Examples** include Ragas, DeepEval, TruLens, Arize Phoenix, Langfuse, Giskard, Braintrust, Galileo, Confident AI, and Tonic Validate (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, custom evaluation metrics, and transparent LLM diagnostics — ideal for ML engineers, AI product teams, and developers building production RAG systems.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Confident AI](https://www.confident-ai.com/)**  
  AI observability and evaluation platform that DeepEval integrates with natively for cloud dashboards, regression testing, and team collaboration. Self-hosting available on Enterprise plans with Terraform modules for AWS, GCP, and Azure, or fully air-gapped deployments. Data never leaves your network — no telemetry, no external license server .

- **[Braintrust](https://www.braintrust.dev/)**  
  Evaluation and observability platform with API-driven function invocation for custom scorers. Supports logging metadata, expected outputs, and scorer results with flexible tracing options .

- **[Galileo](https://www.galileo.ai/)**  
  AI observability platform with Python SDK for trace logging, span management, and evaluation. Supports OpenAI, LangChain, and manual logging patterns with `@log` decorators for workflow, retriever, and tool spans .

- **[Arize Phoenix (Cloud)](https://arize.com/)**  
  Managed version of the open-source Phoenix platform for LLM tracing and evaluation, with enterprise support and hosted infrastructure.

- **[Tonic Validate](https://www.tonic.ai/)**  
  RAG evaluation platform with `ValidateScorer` supporting multiple LLM providers (OpenAI, Claude, Mistral, Cohere, Together AI, AWS Bedrock) and custom metrics for answer consistency and augmentation accuracy .

## Open-Source GitHub Projects

- **[Ragas](https://github.com/explodinggradients/ragas)**  
  **The reference framework for RAG evaluation.** Provides research-backed metrics including Faithfulness, Answer Correctness, Context Precision, Context Recall, Context Entities Recall, Noise Sensitivity, Factual Correctness, Response Relevancy, and Aspect Critique. Includes test set generation for RAG and agentic use cases, CLI (`ragas quickstart`, `ragas evals`, `ragas hello_world`) with templates for RAG, agent, text-to-SQL, and workflow evaluation. Apache 2.0 licensed .

- **[DeepEval](https://github.com/confident-ai/deepeval)**  
  **The pytest for LLMs.** LLM evaluation framework with `deepeval test run` for end-to-end evaluation, GEval for research-backed custom metrics with human-like accuracy, conversational test cases for multi-turn interactions, agent trajectory evaluation with `TaskCompletionMetric`, and `@observe` tracing for LangChain, LangGraph, and OpenAI. Integrates natively with Confident AI for regression testing and cloud dashboards. CLI supports `deepeval login`, `set-confident-region`, `set-local-store`, and `set-mode` for stable vs experimental features .

- **[TruLens](https://github.com/truera/trulens)**  
  Evaluation and observability framework for LLM applications with feedback functions for RAG and agent trace analysis. RAG metrics include **Groundedness** (is response grounded in context?), **Context Relevance**, **Answer Relevance**, and **Coherence**. Agent trace metrics include **Logical Consistency**, **Execution Efficiency**, **Plan Adherence**, **Plan Quality**, **Tool Selection**, and **Tool Calling**. Integrates with MLflow, Pinecone, and LangChain. Open source .

- **[Arize Phoenix](https://github.com/Arize-ai/phoenix)**  
  **Open-source LLM tracing and evaluation.** Run locally (`uvx arize-phoenix serve`), in Docker, or self-hosted with PostgreSQL for persistent storage. Serves UI and OTLP HTTP on port 6006, OTLP gRPC on 4317. `px setup` CLI hands instrumentation to coding agents (Claude Code, Cursor, Codex) and verifies traces actually arrive. Self-hosting guides cover Kubernetes, Helm, Railway, AWS CloudFormation, Google Cloud Run, Azure, and Render. MIT licensed .

- **[Langfuse](https://github.com/langfuse/langfuse)**  
  **Full-platform LLM observability and evaluation.** OpenTelemetry-based tracing with OpenAI and LangChain integrations, datasets & experiments for offline evaluation and regression testing (including CI via GitHub Actions), LLM-as-a-judge and custom evaluations/scores, prompt management, and full REST API client. SDK rewritten in v4 (March 2026). Self-hostable .

- **[Giskard](https://github.com/Giskard-AI/giskard)**  
  **Adversarial RAG diagnostics and red teaming.** `vulnerability_scan` red teams agents with hostile scenarios — prompt injection, jailbreaks, data leakage. `quality_scan` checks answers against your knowledge base to catch **hallucinations, omissions, and refusals to answer**. Generators include AdversarialScenarioGenerator, CrescendoAttackScenarioGenerator, GOATAttackScenarioGenerator, PromptInjectionScenarioGenerator, and GCGInjectionScenarioGenerator. Reproducible with seed control and parallel execution. Quality generators tag scenarios as `component:llm`, `component:retrieval`, or `component:history` for **blame attribution** .

- **[OpenAgent Eval](https://github.com/OpenAgentHQ/openagent-eval)**  
  **Local-first, framework-agnostic RAG and agent evaluation.** No cloud services, dashboards, or authentication required. 18+ metrics across retrieval (Context Precision/Recall, Precision@K, MRR, NDCG), generation (Faithfulness NLI-based, Answer Relevancy, Hallucination Detection, Semantic Similarity, BLEU, ROUGE, BERTScore), and performance (latency, token counting, cost estimation). Includes **Corpus Health Auditor** for detecting contradictions, staleness, and duplicates, **Component Diagnosis** for retrieval vs. generation vs. chunking blame, and **Synthetic Test Data** generation. CLI: `oaeval init`, `run`, `report`, `compare`, `audit`, `diagnose`. Works with OpenAI, Anthropic, Gemini, Groq, OpenRouter, Ollama, and retrievers including Chroma, Qdrant, Pinecone, Weaviate, FAISS, pgvector, Elasticsearch, BM25. Apache 2.0 licensed .

- **[Ragas CLI](https://github.com/explodinggradients/ragas)**  
  Command-line interface for Ragas with templates: `rag_eval` (RAG evaluation), `improve_rag` (naive vs agentic RAG comparison), `agent_evals`, `llamaIndex_agent_evals`, `text2sql`, `workflow_eval`, `prompt_evals`, `judge_alignment`, and `benchmark_llm` .

### Additional Strong Open-Source Options

- **[DeepEval CLI Settings](https://deepeval.com/docs/command-line-interface)** — `deepeval login` for Confident AI integration, `set-confident-region` for data residency (US/EU), `set-local-store` for JSON vs SQLite storage, `set-mode` for stable vs experimental features, `view` to open latest run in browser .
- **[Giskard Scan API](https://docs.giskard.ai/oss/scan/reference/scan-api)** — Programmatic access to `vulnerability_scan()`, `quality_scan()`, `generate_suite()`, and `third_party_scan()` with full control over generators, seed, concurrency, and knowledge base .
- **RAG Evaluation Libraries** — Community implementations of faithfulness, relevance, and hallucination metrics for custom pipelines.
- **Vector Database Evaluation** — Retrieval quality testing for Chroma, Qdrant, Pinecone, Weaviate, and pgvector.

**Frameworks for building custom systems**: Combine **Ragas** for research-backed RAG metrics, **DeepEval** for pytest-style test suites with GEval custom metrics, **TruLens** for groundedness and agent trace scoring, **Arize Phoenix** for self-hosted tracing with PostgreSQL persistence, **Giskard** for adversarial hallucination and prompt injection testing, and **OpenAgent Eval** for local-first corpus auditing and component blame attribution to build a complete self-hosted RAG diagnostics stack.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- RAG diagnostics tools must comply with data protection regulations (GDPR, CCPA), LLM provider terms of service, and organizational data governance requirements. Evaluation metrics are heuristic and may not capture all failure modes — human review remains essential for high-stakes applications.
- Self-hosted open-source solutions require proper infrastructure, LLM API key management, and ongoing validation of evaluation metrics against ground truth.

---

**Made for ML engineers, AI product teams, RAG developers, and teams building reliable LLM applications.**  
Let's make RAG diagnostics more open, rigorous, and production-ready.
