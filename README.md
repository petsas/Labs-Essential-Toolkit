# 🛠️ Health AI Labs Essential Toolkit
 
> A curated reference of all tools presented and discussed at our hack event.
> Use this as a starting point for future hackathons and MVPs.
 
---
 
## 📋 Table of Contents
 
- [Agentic Coding IDEs](#-agentic-coding-ides)
  - [Google Antigravity](#google-antigravity)
  - [OpenAI Codex](#openai-codex)
  - [Claude Code](#claude-code)
- [Quick Prototyping (MVP)](#-quick-prototyping--mvp)
  - [Replit](#replit)
- [Free / Open Models](#-free--open-models)
  - [Mistral](#mistral)
- [Voice Agents](#-voice-agents)
  - [Retell AI](#retell-ai)
  - [ElevenLabs](#elevenlabs)
- [Knowledge Graphs](#-knowledge-graphs)
  - [Graphify](#graphify)
- [Privacy & Depersonalization](#-privacy--depersonalization)
  - [Hugging Face Privacy Filter](#hugging-face-privacy-filter)
- [Local Models (Healthcare & Sensitive Use)](#-local-models-healthcare--sensitive-use)
- [Competitions & Community](#-competitions--community)
- [Key Concepts Discussed](#-key-concepts-discussed)
- [People & Roles](#-people--roles)
---
 
## 🤖 Agentic Coding IDEs
 
### Google Antigravity
 
| | |
|---|---|
| **Website** | [antigravity.google](https://antigravity.google/) |
| **Cost** | Free (public preview for individuals) |
| **Category** | Agentic IDE |
 
**What it does:** Google Antigravity is an AI-native development platform (launched November 2025) that goes beyond autocomplete — it deploys autonomous AI agents that can plan, write code, run terminal commands, and visually test your app in an integrated browser. Think of it as "Mission Control" for your codebase.
 
**Key features:**
- **Editor View** — familiar VS Code-based IDE with AI completions and inline commands
- **Agent Manager (Manager View)** — dispatch up to 5 agents working in parallel on different tasks
- **Artifacts** — agents generate reviewable deliverables (task lists, screenshots, browser recordings) instead of raw tool calls; you can comment directly on them
- **Autonomous browser** — agents can open a built-in Chrome browser to visually test UI
- **Self-improving knowledge base** — saves useful context and code snippets across tasks
- **Multi-model support** — Gemini 3.1 Pro (default), Claude Sonnet/Opus, GPT-OSS 120B
**Best for:** Rapid prototyping, greenfield development, delegating complex multi-step tasks.
 
**Hack tip:** Assign well-scoped missions to multiple agents simultaneously. Let one agent refactor while another writes tests.
 
---
 
### OpenAI Codex
 
| | |
|---|---|
| **Website** | [openai.com/codex](https://openai.com/codex/) |
| **GitHub (CLI)** | [github.com/openai/codex](https://github.com/openai/codex) |
| **Cost** | Included in ChatGPT Plus, Pro, Business, Enterprise |
| **Category** | Agentic coding agent (CLI + cloud + desktop app) |
 
**What it does:** Codex is OpenAI's coding agent for writing features, fixing bugs, answering questions about a codebase, and proposing pull requests — available via CLI (terminal), desktop app, and ChatGPT web. Tasks run in isolated cloud sandboxes preloaded with your GitHub repository.
 
**Key features:**
- **Codex CLI** — open-source, runs locally in your terminal (built in Rust)
- **Codex Cloud** — cloud-based, runs tasks in parallel in sandboxed environments
- **Codex Desktop App** — multi-agent command center for managing long-running tasks
- **Skills** — reusable bundles of instructions + tools for team-specific workflows
- **Automations** — schedule recurring tasks (e.g. issue triage, CI/CD monitoring, PR follow-up)
- **Codex Security** — identifies and proposes fixes for software vulnerabilities (March 2026)
- **IDE integrations** — VS Code, Cursor, Windsurf
**Best for:** Delegating repetitive engineering work, writing tests, refactoring, background automation.
 
**Hack tip:** Use `codex exec` to script and automate repetitive workflows. Combine with MCP servers for integrations.
 
---
 
### Claude Code
 
| | |
|---|---|
| **Website** | [claude.ai/code](https://claude.ai/code) |
| **Docs** | [docs.anthropic.com](https://docs.anthropic.com) |
| **Cost** | Included with Claude API / Claude.ai plans |
| **Category** | Agentic coding agent (CLI) |
 
**What it does:** Claude Code is Anthropic's command-line coding agent that runs in your terminal. It reads your entire codebase, edits files, runs tests, and takes multi-step actions autonomously. It's particularly strong at understanding large codebases and following complex instructions precisely.
 
**Key features:**
- Deep codebase understanding — reads and reasons across entire projects
- Runs terminal commands, edits multiple files, proposes diffs
- MCP (Model Context Protocol) support for tool integrations
- Works alongside your existing git workflow
**Best for:** Complex refactors, understanding unfamiliar codebases, precise multi-file edits.
 
**Hack tip:** Claude Code excels at following nuanced instructions. Write a detailed `AGENTS.md` file in your repo to guide its behavior.
 
---
 
## ⚡ Quick Prototyping / MVP
 
### Replit
 
| | |
|---|---|
| **Website** | [replit.com](https://replit.com) |
| **Cost** | Free tier available; paid plans from ~$20/month |
| **Category** | Cloud IDE + AI app builder |
| **Mentioned as** | "Quick and Dirty" — similar to Lovable |
 
**What it does:** Replit is a browser-based cloud IDE with an AI agent ("Replit Agent") that can build full-stack applications from a text prompt. No local setup required — it spins up an environment, writes code, and hosts your app in one place.
 
**Key features:**
- Zero setup — runs entirely in the browser
- Replit Agent — describe what you want to build, it scaffolds the app
- Instant deployment and hosting
- Collaborative — share and work on projects with others in real time
- Supports 50+ programming languages
**Best for:** Hackathon MVPs, rapid demos, no-setup prototyping.
 
**Hack tip:** Great for "quick and dirty" proofs of concept. Start here to validate an idea before moving to a proper codebase.
 
> **⚠️ Remember to create a codebase** — Replit is great for prototyping but always export/version your code in a proper git repo for anything you want to grow.
 
---
 
## 🆓 Free / Open Models
 
### Mistral
 
| | |
|---|---|
| **Website** | [mistral.ai](https://mistral.ai) |
| **Cost** | Billions of free tokens available (generous free tier) |
| **Category** | LLM provider |
| **Mentioned as** | Comparable to ChatGPT 4.1 — or better |
 
**What it does:** Mistral AI is a European AI company offering powerful open and commercial LLMs. Their models are competitive with GPT-4-class models and are available via API and for local deployment. They offer a very generous free token allowance, making them ideal for hackathons.
 
**Key models:**
- `mistral-large` — flagship, comparable to GPT-4 class
- `mistral-small` — fast and cost-efficient
- `codestral` — specialized for code generation
- `mistral-embed` — for embeddings and RAG
**Why it was highlighted:**
- Massive free token quota — great for hacking without worrying about costs
- Open-weight models available for **local deployment** (no API required)
- Strong multilingual support
- European data residency (important for EU compliance)
**Hack tip:** Use the free API tier for prototyping, then self-host an open-weight Mistral model if you need privacy or offline capability.
 
---
 
## 🎙️ Voice Agents
 
### Retell AI
 
| | |
|---|---|
| **Website** | [retellai.com](https://www.retellai.com) |
| **Docs** | [docs.retellai.com](https://docs.retellai.com) |
| **Cost** | Free $10 credit to start; pay-as-you-go ~$0.07/min |
| **Category** | Voice agent platform |
 
**What it does:** Retell AI is a platform for building, deploying, and managing AI phone agents. It enables low-latency (~600ms), human-quality voice conversations that can handle inbound and outbound calls, book appointments, process payments, and integrate with CRMs — all without rigid scripts.
 
**Two agent types:**
- **Single Prompt** — define a persona and goal in one prompt; the agent handles the rest dynamically
- **Conversation Flow** — structured drag-and-drop conversation design with guardrails for more predictable, script-like flows (reduces hallucinations)
**Key features:**
- ~600ms latency — among the lowest in the industry
- 31+ languages with automatic language detection
- Voice providers: integrates with **ElevenLabs**, OpenAI TTS, and others
- SIP trunking — works with any existing phone infrastructure
- Real-time function calling — agents can book appointments, update records mid-call
- Post-call analytics, sentiment tracking, quality scoring
**Best for:** Customer service automation, healthcare appointment booking, lead qualification, voice-based MVPs.
 
**Hack tip:** Start with the Single Prompt agent for a hackathon — describe your agent's role and it handles conversation flow. Use ElevenLabs for the most realistic voices.
 
---
 
### ElevenLabs
 
| | |
|---|---|
| **Website** | [elevenlabs.io](https://elevenlabs.io) |
| **Cost** | Free tier available |
| **Category** | Text-to-speech / voice synthesis |
 
**What it does:** ElevenLabs provides ultra-realistic AI voice synthesis. It's the leading TTS provider for voice agents, offering voice cloning, multilingual support, and low-latency speech generation. Integrates directly with Retell AI and other voice platforms.
 
**Best for:** Giving your voice agent a realistic, branded voice.
 
---
 
## 🕸️ Knowledge Graphs
 
### Graphify
 
| | |
|---|---|
| **Category** | Knowledge graph / data visualization |
| **Mentioned as** | "Graphify o knowledge graph awl" |
 
**What it does:** Graphify (and similar tools in the knowledge graph space) allows you to visualize and query relationships between data entities as a graph — nodes represent entities (people, concepts, documents) and edges represent relationships between them. This is particularly powerful for RAG (Retrieval-Augmented Generation) systems and complex data exploration.
 
**Use cases:**
- Visualizing connections in research data
- Building semantic search over structured knowledge
- AI-assisted exploration of complex datasets
- Making LLM outputs explainable by grounding them in a knowledge graph
**Related tools to explore:**
- [Neo4j](https://neo4j.com) — leading graph database
- [LlamaIndex](https://www.llamaindex.ai) — has knowledge graph integrations
- [NebulaGraph](https://www.nebula-graph.io) — open-source graph DB
---
 
## 🔒 Privacy & Depersonalization
 
### Hugging Face Privacy Filter
 
| | |
|---|---|
| **Website** | [huggingface.co](https://huggingface.co) |
| **Category** | Privacy / PII removal |
| **Mentioned as** | Alternative to OpenAI's filter for depersonalizing ChatGPT prompts |
 
**What it does:** When sending data to commercial AI APIs (like ChatGPT/OpenAI), there's a risk of sending personally identifiable information (PII) or sensitive data. Hugging Face hosts models and pipelines specifically for:
- **Named Entity Recognition (NER)** — detecting names, addresses, IDs
- **PII redaction** — anonymizing sensitive information before it reaches an API
- **Data anonymization pipelines** — preprocessing data for privacy compliance
**Why it matters for healthcare and enterprise:**
- Allows teams to use powerful cloud LLMs without sending raw patient or user data
- GDPR/HIPAA compliance requirement
- Can be run **locally** (no data leaves your infrastructure)
**Hack tip:** Chain a Hugging Face anonymization model before any API call that processes user data. This is a must-have pattern for healthcare hackathons.
 
---
 
## 🏥 Local Models (Healthcare & Sensitive Use)
 
A key theme of the event: **local AI models matter**, especially in regulated industries.
 
**Why run models locally?**
- Data never leaves your infrastructure — critical for patient data (HIPAA), financial data, legal documents
- No dependency on external APIs — works offline, no rate limits
- Easier compliance with GDPR, HIPAA, and other regulations
- Lower long-term cost at scale
**Recommended local model stacks:**
| Tool | Purpose |
|---|---|
| [Ollama](https://ollama.ai) | Run Mistral, LLaMA, Gemma locally with one command |
| [LM Studio](https://lmstudio.ai) | Desktop GUI for running local models |
| [vLLM](https://github.com/vllm-project/vllm) | High-performance local inference server |
| Mistral (open-weight) | Strong performance, available for self-hosting |
 
**Hack tip:** For a healthcare hackathon MVP, use Ollama + Mistral locally. No data leaves your machine, no API costs, no compliance headaches.
 
---
 
## 🏆 Competitions & Community
 
### Kaggle — Gemma 4 Good Hackathon
 
| | |
|---|---|
| **Website** | [kaggle.com](https://www.kaggle.com) |
| **Model** | Google's Gemma (open-weight LLM) |
 
A hackathon challenge on Kaggle using Google's Gemma model for social good projects. A great opportunity to apply skills from this event in a competitive setting with prizes and visibility.
 
---
 
## 💡 Key Concepts Discussed
 
| Concept | Summary |
|---|---|
| **MVP (Minimum Viable Product)** | Build the smallest version of your idea that proves it works. Ship first, perfect later. |
| **Vibe Coding** | Using AI tools to generate code without deep engineering — fast but needs a solid codebase foundation. |
| **Codebase discipline** | Even when prototyping fast, always maintain a proper git repo. Don't lose your work. |
| **Agentic workflows** | Let AI agents handle multi-step tasks autonomously (coding, browsing, testing) while you supervise. |
| **RAG (Retrieval-Augmented Generation)** | Combining an LLM with a knowledge base/search so it answers from your data, not just training data. |
| **Knowledge graphs** | Structured data as a graph of entities and relationships — powerful for complex, interconnected data. |
| **Local-first AI** | Running AI models on your own hardware — essential for privacy-sensitive sectors like healthcare. |
| **Depersonalization** | Stripping PII from inputs before sending to cloud APIs — a critical privacy pattern. |
 
---
 
## 👥 People & Roles
 
| Name | Role / Affiliation |
|---|---|
| **Alessandro P** | Presenter / Contributor |
| **Antonio** | Presenter / Contributor |
| **Luigi** | Presenter / Contributor |
| **Piergiacomo** | Presenter / Contributor |
| **Nikolas** | Presenter / Contributor |
 
---
 
## 🔗 Quick Links
 
| Tool | Link |
|---|---|
| Google Antigravity | https://antigravity.google |
| OpenAI Codex | https://openai.com/codex |
| Claude Code | https://claude.ai/code |
| Replit | https://replit.com |
| Mistral AI | https://mistral.ai |
| Retell AI | https://retellai.com |
| ElevenLabs | https://elevenlabs.io |
| Hugging Face | https://huggingface.co |
| Ollama (local models) | https://ollama.ai |
| Kaggle | https://kaggle.com |
 
---
 
*Last updated: April 2026 · Maintained by the hack event community*
