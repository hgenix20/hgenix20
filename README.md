# Kameron M. Green

AI engineer. I build agentic systems that hold up in production: orchestration, evaluation, observability, and the guardrails that let an agent touch a system of record.

Ten years shipping automation and AI into regulated enterprise operations. Right now I build production multi-agent LLM systems for enterprise sales operations at **Indeed**. Before that, a decade automating regulated insurance operations, where a sloppy data boundary turns into a compliance finding.

Everything below is public, runnable, and measured.

---

## 🧱 What I build

### [Enterprise Agent Platform](https://github.com/hgenix20/enterprise-agent-platform)
A reference implementation of a production agentic stack, with the architectural decisions written down as ADRs.

- **Model gateway** with provider abstraction, tiered routing by task class, and ordered fallback chains. Measured 100% recovery at **+0.02 ms** added latency with the primary provider failing every call.
- **Tool registry** with MCP-style specs enforcing per-agent authorization. An agent can only call what its grant allows, checked before the tool resolves.
- **Human approval gates** that park a run and resume it durably, exactly-once across processes via atomic compare-and-set on Postgres.
- **Agent memory on pgvector**, per-agent scoping enforced in the query. 1.05 ms ranked search at k=5.
- LangGraph orchestration, OpenTelemetry spans on every model call and tool execution, a 6-case eval suite gating CI, 45 tests, 6 ADRs.
- **Kubernetes deploy verified** on k3d: 100/100 runs at 5.4 ms mean end to end with durable persistence, every row confirmed in the cluster database.

Benchmarks and method notes are published in [`docs/benchmarks.md`](https://github.com/hgenix20/enterprise-agent-platform/blob/main/docs/benchmarks.md).

### [SignalNodus](https://github.com/hgenix20/signalnodus) · [signalnodus.ai](https://signalnodus.ai)
A live SEC-filing intelligence API with a **public evaluation suite**: 88 published test cases with accuracy reporting, a usage audit log, and per-request receipts. You shouldn't have to trust a system you can't inspect. Sole builder and operator.

### [ModelProof](https://github.com/hgenix20/modelproof)
A dual-LLM output verifier. A verifier model adjudicates a primary model's outputs for hallucination, bias, and intent alignment before they reach the user, and the user gets a confidence report alongside the answer.

**Microsoft AI Agents Hackathon 2025, category winner (Best JavaScript/TypeScript Agent), $5,000.** The hackathon drew 18,000+ registered participants and 570 project submissions across seven categories. [Category winners showcase](https://techcommunity.microsoft.com/blog/azuredevcommunityblog/ai-agents-hackathon-2025-%E2%80%93-category-winners-showcase/4415088)

### [pokeai](https://github.com/hgenix20/pokeai)
A symbolic, long-horizon agent that plays Pokémon FireRed end to end through the BizHawk emulator with **no game API**. Perception is deterministic, read live from emulator RAM, which makes grounding a real problem. Hierarchical planning and navigation, a fact-gated storyline dispatcher that resumes from any save state, pluggable strategies, and a live operator dashboard.

Built as much as a reproducible evaluation environment as an agent: ~765 automated tests across perception, planning, battle logic, pathing, and the story dispatcher. Actively developed, full-playthrough coverage still on the roadmap.

### [HCQM](https://github.com/hgenix20/hcqm)
An open, 8-domain framework for measuring AI capability and reliability, spanning cognitive, executive, emotional/social, creative, motivational, learning, digital, and systems intelligence.

**v1.0 published**, archived on Zenodo with a resolving DOI: [10.5281/zenodo.20668273](https://doi.org/10.5281/zenodo.20668273), mirrored to Software Heritage. In external review with researchers in cognitive architecture, AI evaluation, and psychometrics, including the Institute for Applied Psychometrics, whose director is named in the paper's acknowledgments. Portfolio research, not peer-reviewed.

It started as a tool I built to assess and develop my daughter's capabilities holistically. It became clear the same structure could work as an architectural blueprint for AI systems that mirror how human cognition is organized.

---

## 🛠️ Stack

**Languages** Python · TypeScript / Node.js · SQL

**Agentic AI** multi-agent orchestration · LangGraph · LangChain · MCP · A2A · tool calling and tool registries · per-agent authorization · agent memory · planning loops · structured outputs · retries and failure recovery · human-in-the-loop approval gates

**LLM systems** RAG · embeddings and vector search · model gateways · tiered routing and ordered fallback · token and cost telemetry · Anthropic · OpenAI-compatible APIs · Azure OpenAI

**Evaluation & observability** offline and regression eval suites · evals as CI quality gates · hallucination detection and output verification · OpenTelemetry · distributed tracing · latency and cost benchmarking

**Backend & data** FastAPI · REST APIs · async and concurrent Python · PostgreSQL · pgvector · Redis · MongoDB · Snowflake

**Infrastructure** Docker · Kubernetes · GitHub Actions · GitLab CI/CD · Cloudflare Workers · AWS / Azure / GCP

**Enterprise integration** n8n · Salesforce (Flow / Apex / Aura) · MuleSoft · Blue Prism · UiPath · Power Automate

---

## 🎓 Education

- **M.S. Computer Science, concentration in Artificial Intelligence** · University of Nebraska at Omaha *(in progress, expected 2027)*
- **B.S.B.A. Economics** · University of Nebraska at Omaha · 2024

---

## 📚 What I'm thinking about

- Cognitive architecture for LLM-based agents
- Long-horizon agent systems and memory architectures
- Evaluation that catches the failure you didn't predict, not the one you wrote the test for
- The gap between descriptive capability frameworks and prescriptive engineering blueprints
- Reliability that survives a model swap

---

## 🤝 Connect

I welcome substantive engagement from people working on adjacent problems, particularly agent reliability, evaluation, cognitive architecture, and getting AI past enterprise governance.

- 📧 **Email:** kameron.m.green@outlook.com
- 💼 **LinkedIn:** [linkedin.com/in/kameronmgreen](https://www.linkedin.com/in/kameronmgreen/)
- 𝕏 **X:** [@KameronMGreen](https://x.com/KameronMGreen)
- 🆔 **ORCID:** [0009-0002-8350-3641](https://orcid.org/0009-0002-8350-3641)
- 🎓 **Academic:** kgreen@unomaha.edu

---

*Building in public.*
