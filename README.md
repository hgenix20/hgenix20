# Kameron M. Green

**AI Product Engineer**

I design and build production AI systems end to end, and I ship them in public. I build multi-agent LLM systems; opportunities they created have closed won by the hundreds, for tens of millions of dollars, since launch in early 2026. Next I'm aiming AI at harder problems, starting with quantum circuit compilation for fusion energy.

## Products and systems

### [ModelProof](https://github.com/hgenix20/modelproof)
Two models answer each prompt in parallel, and a third scores every reply for hallucination, bias, toxicity and intent match in a panel beside the chat. Built solo.
**Microsoft AI Agents Hackathon 2025, category winner (Best JavaScript/TypeScript Agent), $5,000**, from 570 submissions and 18,000+ registered participants. [Winners showcase](https://techcommunity.microsoft.com/blog/azuredevcommunityblog/ai-agents-hackathon-2025-%E2%80%93-category-winners-showcase/4415088)

### [Agent Room](https://github.com/hgenix20/agent-room) · [live](https://room.kamerongreen.dev)
A shared channel and task board where people and AI agents coordinate work, with token estimates against actuals for every task. Cloudflare Workers, Durable Objects, WebSockets and Cloudflare Access. 140 tests; deploys on every push.

### [SignalNodus](https://github.com/hgenix20/signalnodus)
A paid SEC-filing API built for AI agents, which I built and ran in 2026. It had 31 tools over REST and MCP, was listed in the official MCP registry, and billed per call through Stripe and x402. Every answer carried its accession number, filing date and parser version, so an amended filing couldn't change a pinned result, and its accuracy was published on an 88-case public test set. Retired in September 2026.

### [Enterprise Agent Platform](https://github.com/hgenix20/enterprise-agent-platform)
The core of a production agent stack, with every major decision written down as an ADR. A model gateway routes by task tier with ordered fallback. A tool registry checks each agent's permissions before a tool resolves. Human approval steps pause a run and resume it exactly once across processes. Memory runs on pgvector, and tracing on OpenTelemetry. Deployed on Kubernetes (k3d), where the rollout exposed a startup race that I fixed. 45 tests, [benchmarks with method notes](https://github.com/hgenix20/enterprise-agent-platform/blob/main/docs/benchmarks.md).

### Genix Mind *(private)*
A persistent autonomous agent that I run on its own Linux server. I measured its context growing from 47k to 818k tokens per response and built deterministic compaction at a 300k bound. I root-caused an out-of-memory outage and fixed it at three levels, and I built a monitoring hub whose restart command drains work, reboots the host and resumes every agent. It's proven through a real reboot. About 1,300 tests. Operations layer demoable on request.

### Agents for games and puzzles
- [arc3-mind-agent](https://github.com/hgenix20/arc3-mind-agent): offline agent for the ARC-AGI-3 Kaggle competition on a locally served model; paper-track writeup submitted November 2026. A second design, [arc3-curiosity-agent](https://github.com/hgenix20/arc3-curiosity-agent), is published with its results and failure analysis.
- [pokeai](https://github.com/hgenix20/pokeai): plays Pokémon FireRed with no game API by reading and decrypting emulator memory, and resumes from any save state. 445 tests, CI on Python 3.10 to 3.12.

Also: [ai-eval-platform](https://github.com/hgenix20/ai-eval-platform), a test harness with a CI gate and published measurements (318 tests).

## Now
- Quantum circuit compilation for the Google Quantum AI challenge on Kaggle: a fusion-energy subroutine, scored on qubits and gate counts. Verified baseline reproduced; optimizing.
- M.S. in Computer Science (AI), University of Nebraska at Omaha, expected 2027.

## Research
[HCQM v1.0](https://github.com/hgenix20/hcqm), an open capability framework across 8 domains. Archived on Zenodo: [10.5281/zenodo.20668273](https://doi.org/10.5281/zenodo.20668273).

## Stack
**Languages:** Python · TypeScript · SQL
**AI:** Anthropic and OpenAI-compatible APIs · Azure OpenAI · LangGraph · MCP · multi-agent orchestration · context engineering · RAG
**Backend and data:** FastAPI · PostgreSQL · pgvector · Redis · MongoDB · Cloudflare D1
**Infrastructure:** Cloudflare Workers and Durable Objects · Docker · Kubernetes · Linux and systemd · GitHub Actions · OpenTelemetry

## Contact
[LinkedIn](https://www.linkedin.com/in/kameronmgreen/) · [kamerongreen.dev](https://kamerongreen.dev) · [X @KameronMGreen](https://x.com/KameronMGreen) · [ORCID](https://orcid.org/0009-0002-8350-3641) · kameron.m.green@outlook.com
