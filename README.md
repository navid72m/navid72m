# Navid Mirnouri — AI Systems Engineer

**Agent reliability & security · Retrieval systems · Low-level ML performance**

I build the unglamorous layer that makes AI systems trustworthy: runtime security auditing for agent tooling, vector search engines written from scratch in C, and agentic frameworks with deterministic backstops instead of prompt hope. Background in distributed backends at scale (1M+ MAU in Go, high-throughput IoT pipelines) and an M.Sc. in Informatics from TUM.

---

## Featured work

| Project | What it is | Links |
|---|---|---|
| **mcp-behave** | Runtime behavioral security auditor for MCP servers. Traces actual syscalls via strace to catch undeclared file/network/process activity, permission-scope violations, and post-install "rug-pull" manifest changes (hash pinning). CI-ready `--json` / `--fail-on` modes. | [repo](https://github.com/navid72m/mcp-behave) · [PyPI](https://pypi.org/project/mcp-behave/) |
| **vecdb** | A from-scratch C11 vector database: HNSW + Vamana (DiskANN-style) graph indexes, SIMD distance kernels (AVX-512 / NEON), 4-/8-bit TurboQuant compression, filtered search, Python bindings. Benchmarked against FAISS on SIFT1M/GIST1M. | [repo](https://github.com/navid72m/vectorDatabase) · [PyPI](https://pypi.org/project/vecdbc/) |
| **AgentForge** | Local-first, low-code framework that generates LangGraph agentic systems from natural language — with deterministic validation backstops, because "the prompt says don't" is not an architecture. | [repo](https://github.com/navid72m/AgentForge) |
| **AdaptiveRAG** | Self-configuring agentic RAG framework on LangGraph/Ollama: inspects your corpus and query patterns, then picks its own retrieval strategy. | [repo](https://github.com/navid72m/adaptiveRAG) · [PyPI](https://pypi.org/project/adaptiverag/) |
| **pdf** | Document intelligence platform combining semantic embedding, intelligent retrieval, and generation for end-to-end document Q&A. | [repo](https://github.com/navid72m/pdf) |

**Also:** an ARM NEON ternary GEMM kernel for BitNet-style 1.58-bit inference sustaining 40+ GOP/s on Apple Silicon (with roofline analysis), and a bilingual (English/Persian) production voice agent on Deepgram + Cloudflare Workers.

---

## How I got here

Systems engineering first, AI second — in the order that makes AI systems actually work. Scaled Go backends to 1M+ monthly active users at Quiz of Kings, built serverless IoT platforms managing 100k+ devices at MDOP, and engineered ML-supporting data pipelines with 99.9% reliability at Node-h (Munich). That foundation is why my AI projects ship with write-ahead logs, benchmarks, and CI flags rather than just demos.

## The thread underneath

I care about the nature of intelligence, not just its applications. [Noesis](https://github.com/navid72m/Noesis) is a local-first research framework for studying memory, self-modeling, and phenomenological behavior in LLMs; [sim-society](https://github.com/navid72m/sim-society) simulates societies of LLM agents to study deliberation, fairness, and value alignment. The engineering discipline and the philosophy of mind interest are the same project viewed from two sides: if you want to understand a mind, try to build the architecture that could support one.

---

## Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-navid--mirnouri-0077B5?style=flat-square&logo=linkedin)](https://linkedin.com/in/navid-mirnouri)
[![Email](https://img.shields.io/badge/Email-navid72m%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:navid72m@gmail.com)
[![PyPI](https://img.shields.io/badge/PyPI-navid72m-3775A9?style=flat-square&logo=pypi&logoColor=white)](https://pypi.org/user/navid72m/)

Open to roles in agent infrastructure, AI reliability/security, and retrieval systems.
