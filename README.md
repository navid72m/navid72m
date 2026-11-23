<p align="center">
  <img src="navid-coding-banner.png" alt="Navid Mirnouri — AI Systems Engineer" width="100%" />
</p>

<h1 align="center">Navid Mirnouri</h1>

<p align="center">
  <strong>AI Systems Engineer</strong><br />
  Agent Runtime Security · Retrieval Systems · Low-Level ML Performance
</p>

<p align="center">
  <a href="https://linkedin.com/in/navid-mirnouri">
    <img src="https://img.shields.io/badge/LinkedIn-navid--mirnouri-0077B5?style=flat-square&logo=linkedin" alt="LinkedIn" />
  </a>
  <a href="mailto:navid72m@gmail.com">
    <img src="https://img.shields.io/badge/Email-navid72m%40gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" />
  </a>
  <a href="https://pypi.org/user/navid72m/">
    <img src="https://img.shields.io/badge/PyPI-navid72m-3775A9?style=flat-square&logo=pypi&logoColor=white" alt="PyPI" />
  </a>
</p>

---

I build the unglamorous infrastructure layer that makes AI systems trustworthy: runtime monitoring and security proxies for agent tooling, vector search engines written from scratch in C, and agentic frameworks backed by deterministic enforcement instead of prompt hope. Background in distributed backends at scale (1M+ MAU in Go, high-throughput IoT pipelines) and an M.Sc. in Informatics from TUM.

---

## Flagship Project — [`mcp-behave`](https://github.com/navid72m/mcp-behave)

> **Observe. Enforce. Trust.** — Runtime visibility, behavioral auditing, and security proxy for Model Context Protocol (MCP) servers.

<p align="center">
  <a href="https://github.com/navid72m/mcp-behave">
    <img src="https://img.shields.io/badge/GitHub-mcp--behave-0B1220?style=for-the-badge&logo=github&logoColor=00E5FF" alt="mcp-behave GitHub" />
  </a>
  <a href="https://pypi.org/project/mcp-behave/">
    <img src="https://img.shields.io/badge/PyPI-mcp--behave-0B1220?style=for-the-badge&logo=pypi&logoColor=2EE59D" alt="mcp-behave PyPI" />
  </a>
</p>

<p align="center">
  <img
    src="https://raw.githubusercontent.com/navid72m/mcp-behave/main/docs/assets/mcp-behave-architecture.gif"
    alt="mcp-behave runtime monitoring and security proxy architecture"
    width="100%"
  />
</p>

`mcp-behave` sits inline between an MCP Client and MCP Server over bidirectional stdio JSON-RPC streams, separating protocol enforcement, best-effort OS telemetry, and optional containment into explicit architectural layers:

| Layer | Responsibility |
| :--- | :--- |
| **Inline MCP Proxy** | Monitors JSON-RPC messages and tool calls, enforces approved tool/request policies, and periodically re-verifies server manifests (`tools/list` hash pinning) to surface post-install "rug-pull" capability changes. |
| **Response Protection** | Independently scans server responses for canaries and sensitive data, supporting secret redaction before responses return to the client. |
| **Native Tracing (Separate Path)** | Runs a non-blocking, best-effort native interposer (`MCP Server → Native Interposer → TracerServer`) to observe selected file, network, and process activity outside the JSON-RPC stream. |
| **Attribution & Audit Reporting** | Correlates protocol events and native telemetry into structured audit reports with findings, evidence, severity, and explicit confidence/coverage limitations—plus CI-ready `--json` and `--fail-on` modes. |
| **Optional Sandbox Containment** | Decoupled containment boundary around the MCP Server, kept distinct from observation so visibility and enforcement guarantees remain transparent. |

---

## Selected Systems & AI Projects

| Project | Focus | Highlights | Links |
| :--- | :--- | :--- | :--- |
| **[`vecdb`](https://github.com/navid72m/vectorDatabase)** | Retrieval & C11 | From-scratch C11 vector database with HNSW + Vamana (DiskANN-style) graph indexes, AVX-512 / ARM NEON SIMD distance kernels, 4-/8-bit TurboQuant compression, filtered search, and Python bindings. Benchmarked against FAISS on SIFT1M/GIST1M. | [Repo](https://github.com/navid72m/vectorDatabase) · [PyPI](https://pypi.org/project/vecdbc/) |
| **[`AgentForge`](https://github.com/navid72m/AgentForge)** | Agent Reliability | Local-first, low-code framework that compiles natural language into LangGraph agentic systems with deterministic validation backstops—because *"the prompt says don't"* is not an architecture. | [Repo](https://github.com/navid72m/AgentForge) |
| **[`AdaptiveRAG`](https://github.com/navid72m/adaptiveRAG)** | Agentic Retrieval | Self-configuring RAG framework on LangGraph/Ollama that inspects corpus characteristics and query patterns to select its own retrieval strategy. | [Repo](https://github.com/navid72m/adaptiveRAG) · [PyPI](https://pypi.org/project/adaptiverag/) |
| **[`pdf`](https://github.com/navid72m/pdf)** | Document AI | End-to-end document intelligence pipeline combining semantic embedding, retrieval, and grounded generation for document Q&A. | [Repo](https://github.com/navid72m/pdf) |

**Also built:**
- **ARM NEON Ternary GEMM Kernel** — BitNet-style 1.58-bit inference kernel sustaining **40+ GOP/s** on Apple Silicon, complete with roofline analysis.
- **Bilingual Production Voice Agent** — Real-time English/Persian voice agent built on **Deepgram + Cloudflare Workers**.

---

## Engineering Background

**Systems engineering first, AI second** — in the order that makes AI systems actually hold up in production.

- **Quiz of Kings** — Scaled Go backends to **1M+ monthly active users**.
- **MDOP** — Built serverless IoT platforms managing **100k+ connected devices**.
- **Node-h (Munich)** — Engineered ML-supporting data pipelines maintaining **99.9% reliability**.
- **TU Munich (TUM)** — M.Sc. in Informatics.

That foundation is why my AI repositories ship with write-ahead logs, roofline benchmarks, explicit threat-model boundaries, and CI exit flags instead of notebook demos.

---

## The Thread Underneath

I care about the nature of intelligence, not just its applications:

- **[`Noesis`](https://github.com/navid72m/Noesis)** — Local-first research framework for studying memory, self-modeling, and phenomenological behavior in LLMs.
- **[`sim-society`](https://github.com/navid72m/sim-society)** — Multi-agent LLM society simulator for studying deliberation, fairness, and value alignment.

The systems discipline and the philosophy of mind interest are the same project viewed from two sides: if you want to understand a mind, try to build the architecture that could support one.

---

<p align="center">
  <strong>Open to roles in agent infrastructure, AI reliability &amp; security, and retrieval systems.</strong><br /><br />
  <a href="https://linkedin.com/in/navid-mirnouri">LinkedIn</a> ·
  <a href="mailto:navid72m@gmail.com">navid72m@gmail.com</a> ·
  <a href="https://pypi.org/user/navid72m/">PyPI</a>
</p>
