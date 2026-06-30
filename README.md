# Engineering Portfolio

AI/LLM work in private repositories.

## Projects

- **LLM Benchmark Suite** — 7 benchmark types (intelligence across 9 domains, agentic tool use, judge ranking absolute and pairwise, throughput, max-context multi-needle retrieval), multi-provider via LiteLLM abstraction, custom eval-harness with resume/retry and cache layer.

- **rag-lab** — Multi-tenant RAG system for confidential documents. Three-layer egress guard with Argon2-hashed scoped bearer tokens, audit log, tenant collections. Composable retrieval pipeline with dense search, MMR, cross-encoder reranking, and query decomposition.

- **QLoRA Fine-Tuning** — German clinical PII extraction from laboratory reports. F1 strict 0.962 in-domain on the ai4privacy corpus. Local M1 Ultra training.

- **Agentic CLI** — 50+ tools in daily use, unified tool calling across cloud LLMs and local models, plus MCP integration. Built from scratch because standard tools are either not private enough or carry too much prompt overhead for local inference.

- **Reporting Engine** — Secure-by-design pipeline with two-tier data classification (confidential / unrestricted) and model whitelisting. Confidential data exclusively via local Ollama, anonymized data and metadata via cloud LLM.

## Engineering Convictions

- **Privacy-by-design.** Sensitive data routed to local models, only sanitized data sees the cloud.
- **Eat my own dogfood.** Tools built for real workflow needs and used daily.
- **Eval and observability from day one.** If you can't measure it, you can't trust it in production.
- **Multi-provider abstraction over vendor lock-in.** LiteLLM, MCP, swap any model in/out.
- **Prefer composition over framework lock-in.** Small, testable components, explicit data flow.
