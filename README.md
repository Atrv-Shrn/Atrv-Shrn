# Atharva Sheoran

**AI Engineer** — I build autonomous agent systems and the eval harnesses that prove they work.

An agent trusted with commit access that no reasoning failure can turn destructive. A question-answering service graded on knowing when *not* to answer. Everything below is self-hosted, documented, and measured — and every README explains why it's built that way, including which parts are mine and which the framework's.

🟢 **Open to part-time contract work** — 20–28 hrs/week, async-first, with a daily overlap window covering EU afternoons and US-East mornings.

---

## Projects

### 📚 [Obsidian-Librarian](https://github.com/Atrv-Shrn/Obsidian-Librarian)

An AI librarian for your notes. Ask it anything about your Obsidian vault and it answers from the actual files with clickable `[[wikilink]]` citations — or tells you it doesn't know. Ask it to *do* something and it drafts the change, shows you, and waits for your yes.

A RAG pipeline and a LangGraph agent welded together in one container. The retrieval half physically cannot write; every edit is proposed for confirmation first.

**▶️ [Watch the demo](https://github.com/Atrv-Shrn/Obsidian-Librarian/blob/main/assets/demo.mp4)** · `LangGraph` `LlamaIndex` `Qdrant` `MCP` `Docker`

### 🩹 [MendBot](https://github.com/Atrv-Shrn/MendBot)

A self-hosted GitHub App that reviews your pull requests as an autonomous agent and pushes safe fixes when it finds them. No fixed pipeline — it decides for itself whether to read more context, comment, fix, or leave the code alone.

Safe to hand commit access because safety lives in the tools, not the prompt: it edits only files already in the diff, on the PR's own branch, under line caps — and edits land as one commit at the very end, so a crashed run writes nothing. Graded against a golden set of real PRs with known answers: **4/4 at baseline** on the fix-or-don't decision, including declining two fixes that looked safe but weren't.

`LangGraph` `LangChain` `Langfuse` `FastAPI` `Docker`

### 🔍 [Anthropic-RAG](https://github.com/Atrv-Shrn/Anthropic-RAG)

Grounded Q&A over the docs, issues and PRs of Anthropic's two SDK repos, refreshed hourly and served to AI agents over MCP.

Built to **abstain** — when the sources can't support an answer it refuses instead of guessing, and the eval set includes out-of-scope questions to measure exactly that. Pairs semantic with keyword search, because developer questions hinge on the exact tokens vector search blurs. Runs without a GPU.

`LlamaIndex` `Qdrant` `Redis` `MCP` `RAGAS` `Docker`

### 🦅 [Kestrel](https://github.com/Atrv-Shrn/Kestrel-Openclaw) & 🌌 [Cosmo](https://github.com/Atrv-Shrn/Cosmo-Openclaw)

Agents that extend themselves. When Kestrel hits a task it can't do yet, it finds or builds the missing tool and keeps it for next time, delegating every code change to a coding sub-agent. Cosmo runs proactive startup ops on a heartbeat, with skills that evolve as it works.

`OpenClaw` `MCP` `Claude Code`

### 🏛️ [Socrates-Qwen3-8B](https://huggingface.co/AthrvShrn/Socrates-Qwen3-8B)

A Qwen3-8B fine-tune that reasons Socratically in its `<think>` trace — clarify the question, define terms, test counterexamples — before answering with stated confidence, or admitting the question can't be settled. Hand-written training set, held-out split, measured before-vs-after. [Quantized builds](https://huggingface.co/AthrvShrn/Socrates-Qwen3-8B-GGUF) run in one command.

`QLoRA` `Unsloth` `GGUF` `Ollama`

---

## Writing

**[Building Software That Isn't Just AI Slop](https://github.com/Atrv-Shrn/Atrvs-SDD)** — the spec-driven method I use to ship working software with coding agents. Four principles, and why the winning setup is the boring one.

---

## Stack

| | |
|---|---|
| **Agents** | LangGraph · LangChain · MCP · tool design & guardrails · human-in-the-loop |
| **RAG** | LlamaIndex · Qdrant · Redis · hybrid search · reranking · incremental ingestion |
| **Evals & observability** | Langfuse · RAGAS · golden sets · LLM-as-judge |
| **Serving & infra** | Python · FastAPI · Docker · GitHub Apps & webhooks |
| **Fine-tuning** | QLoRA (Unsloth) · GGUF export · Ollama |

---

## Reach me

[Email](mailto:atharvasheoran@gmail.com) · [LinkedIn](https://www.linkedin.com/in/atharva-sheoran/) · [Hugging Face](https://huggingface.co/AthrvShrn)

<sub>Self-taught. Every project above was built independently.</sub>
