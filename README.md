# Atharva Sheoran

**AI Engineer** | AI agents, RAG pipelines, agentic workflows, LLM fine-tuning, n8n
**Stack:** LangChain · LangGraph · LlamaIndex · MCP · Qdrant · FastAPI · Docker

What I build:

- AI agents that take real actions, with guardrails in the tools rather than the prompt
- RAG pipelines that cite their sources and abstain instead of guessing
- Agentic workflows and always-on ops agents
- Evals: golden sets, adversarial suites, tracing

🟢 **Open to full-time, contract or part-time work.** Up to 40 hrs/week, async-first, daily overlap window covering EU afternoons and US-East mornings.

---

## Projects

### 📚 [Obsidian-Librarian](https://github.com/Atrv-Shrn/Obsidian-Librarian)

RAG pipeline and LangGraph agent over an Obsidian vault, in one container. Answers from the actual files with clickable `[[wikilink]]` citations, or says it does not know. Every edit is proposed for confirmation first; the retrieval half physically cannot write.

210 unit tests. 10/10 on the golden set at 0.97 faithfulness. 15 adversarial scenarios survived, including a defeated prompt injection.

**▶️ [Watch the demo](https://github.com/Atrv-Shrn/Obsidian-Librarian/blob/main/assets/demo.mp4)** · `LangGraph` `LlamaIndex` `Qdrant` `Redis` `SQLite` `MCP` `Docker`

### 🩹 [MendBot](https://github.com/Atrv-Shrn/MendBot)

Self-hosted GitHub App. Autonomous PR review agent that pushes safe fixes. No fixed pipeline: it decides whether to read more context, comment, fix, or leave the code alone.

Safe to give commit access because safety lives in the tools, not the prompt. Edits only files already in the diff, on the PR's own branch, under line caps, landed as one commit at the end, so a crashed run writes nothing.

4/4 at baseline on a golden set of real PRs, including two correct declines on fixes that looked safe.

`LangGraph` `LangChain` `Langfuse` `FastAPI` `Docker`

### 🔍 [Anthropic-RAG](https://github.com/Atrv-Shrn/Anthropic-RAG)

Grounded Q&A over the docs, issues and PRs of Anthropic's two SDK repos. Hourly incremental ingestion. Served to AI agents over MCP.

Abstains when the sources cannot support an answer. Hybrid dense and sparse retrieval with reranking, because developer questions hinge on exact tokens. Three stores: Qdrant for fused vectors, Redis for verbatim markdown so citations are exact, SQLite for sync state. Runs without a GPU.

`LlamaIndex` `Qdrant` `Redis` `SQLite` `MCP` `Docker`

### 🦅 [Kestrel](https://github.com/Atrv-Shrn/Kestrel-Openclaw) & 🌌 [Cosmo](https://github.com/Atrv-Shrn/Cosmo-Openclaw)

Agents that extend themselves. Kestrel finds or builds the tool it is missing and keeps it for next time, delegating every code change to a coding sub-agent.

Cosmo ran around the clock on **AWS EC2**: 30-minute heartbeat, website health checks, cron daily digest, Vercel deployment monitoring, team Telegram channel. It repaired a production site end to end unattended: detected the outage, spun up a coding agent, diagnosed, fixed, reviewed, redeployed.

`OpenClaw` `MCP` `Claude Code` `AWS EC2` `cron`

### 🏛️ [Socrates-Qwen3-8B](https://huggingface.co/AthrvShrn/Socrates-Qwen3-8B)

QLoRA fine-tune of Qwen3-8B that reasons Socratically inside its `<think>` trace: clarify the question, define terms, test counterexamples, then answer with stated confidence. 136 hand-authored training examples, 109 train / 27 held out, [published openly as a dataset](https://huggingface.co/datasets/AthrvShrn/Socratic-Reasoning). [Quantized builds](https://huggingface.co/AthrvShrn/Socrates-Qwen3-8B-GGUF) run in one command, 400+ downloads a month.

`QLoRA` `Unsloth` `GGUF` `Ollama`

---

## Writing

**[Building Software That Isn't Just AI Slop](https://github.com/Atrv-Shrn/Atrvs-SDD)**: the spec-driven method I use to ship working software with coding agents. Four principles, and why the winning setup is the boring one.

---

## Stack

| | |
|---|---|
| **Agents** | LangGraph · LangChain · MCP · tool design & guardrails · human-in-the-loop |
| **RAG** | LlamaIndex · Qdrant · Redis · hybrid search · reranking · incremental ingestion |
| **Automation** | n8n · webhooks · cron · scheduled agents |
| **Testing & observability** | Langfuse · RAGAS · golden sets · adversarial testing |
| **Serving & infra** | Python · FastAPI · Docker · GitHub Apps & webhooks |
| **Deployment & ops** | AWS EC2 · Linux server admin · cron · Vercel · health checks & automated recovery |
| **Fine-tuning** | QLoRA (Unsloth) · GGUF export · Ollama |

---

## Reach me

[Email](mailto:atharvasheoran@gmail.com) · [Hugging Face](https://huggingface.co/AthrvShrn)

<sub>Self-taught. Every project above was built independently.</sub>
