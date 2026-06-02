# How Deploy AI Models with [vLLM](https://vllm.ai/) <!-- omit in toc -->

---
## Table of Contents <!-- omit in toc -->
- [Abstract](#abstract)
- [Author, Affiliation and Contact](#author-affiliation-and-contact)
- [General Aim](#general-aim)
- [Particular Aims](#particular-aims)
- [Tech Stack and General Knowledge](#tech-stack-and-general-knowledge)
  - [vLLM](#vllm)
  - [LangChain Ecosystem](#langchain-ecosystem)
  - [Open WebUI](#open-webui)
- [Methodology](#methodology)
  - [AI Usage](#ai-usage)
  - [Relevant Parameters for vLLM](#relevant-parameters-for-vllm)
- [Installation and Usage](#installation-and-usage)
- [Experiments](#experiments)
- [License](#license)


---
## Abstract


---
## Author, Affiliation and Contact
Alexis Aguilar [Student of Bachelor's Degree in "Tecnologías para la Información en Ciencias" at Universidad Nacional Autónoma de México [UNAM](https://www.unam.mx/)]: alexis.uaguilaru@gmail.com

Project developed for the subject "Neural Networks 2" taught in semestre 2026-2.


---
## General Aim
Develop a minimal, **end-to-end solution to deploy and serve local LLMs** using [vLLM](https://vllm.ai/) as the core inference engine.


---
## Particular Aims
* Configure and deploy the base vLLM engine instance, integrating a real-time monitoring with [Grafana](https://grafana.com/) to track key production metrics.
* Connect [Open WebUI](https://openwebui.com/) to the vLLM OpenAI-compatible endpoint to establish an intuitive, chat-based interface.
* Orchestrate a production-grade AI agent leveraging the [LangChain ecosystem](https://www.langchain.com/), using LangGraph Platform for stateful logic and LangSmith for execution tracing.


---
## Tech Stack and General Knowledge

### [vLLM](https://vllm.ai/)
* **High-throughput inference engine**: Serve SOTA LLMs with efficient management of attention KV memory via [PagedAttention](https://vllm.ai/blog/2023-06-20-vllm).
* **Flexible Quantization**: Support for [on-the-fly/online techniques](https://docs.vllm.ai/en/latest/features/quantization/online/) and pre-quantized formats [(AWQ, GGUF, compressed-tensors)](https://docs.vllm.ai/en/latest/features/quantization/) to minimize VRAM footprint.
* **Kernel Optimization**: Leverage advanced attention kernels like FlashAttention and FlashInfer to maximize inference speed and hardware efficiency.
* **OpenAI Ecosystem**: Expose an [OpenAI-compatible API](https://bentoml.com/llm/model-interaction/openai-compatible-api), ensuring seamless drop-in integration with UI clients and agentic frameworks.
* **Hardware Agnostic**: Broad support across diverse [GPU architectures](https://docs.vllm.ai/en/latest/getting_started/installation/gpu/) (NVIDIA, AMD, Intel, etc.).
* **Dynamic Multi-LoRA**: Native capabilities to [integrate and swap multiple](https://docs.vllm.ai/en/latest/features/lora/) [LoRA adapters](https://huggingface.co/papers/2106.09685) concurrently on a single base model without sacrificing batching performance.

### [LangChain Ecosystem](https://www.langchain.com/)
* **AI Agent and Components Abstraction ([LangChain](https://docs.langchain.com/oss/python/langchain/overview))**: A robust orchestration library providing [standardized interfaces](https://reference.langchain.com/python/langchain) for prompts, memory, document loaders, and tools.
* **Stateful Multi-Agent Orchestration ([LangGraph](https://docs.langchain.com/oss/python/langgraph/overview))**: Built as a graph-based framework to model complex, cyclic, and non-linear agent behaviors as state machines, featuring native persistence, multi-agent cooperation, and Human-in-the-loop intervention points.
* **Advanced LLM Observability ([LangSmith](https://docs.langchain.com/langsmith/home)/[LangGraph](https://docs.langchain.com/oss/python/langgraph/overview)+[LangFuse](https://langfuse.com/))**: Offers end-to-end telemetry and execution tracing to visually debug prompts, profile step-by-step latency, inspect tool invocations, and log token consumption.
* **Provider Agnostic Ecosystem**: Inherently compatible with local high-performance backends (like vLLM or Ollama) and cloud enterprise providers (OpenAI, Anthropic) via unified wrapper classes.

### [Open WebUI](https://openwebui.com/)
* **ChatGPT-like UI**: A self-hosted, highly responsive, and feature-rich user interface designed for seamless interaction with [local and cloud AI](https://docs.openwebui.com/getting-started/quick-start/connect-a-provider/) solutions.
* **Drop-in OpenAI Compatibility**: Seamless integration with any [OpenAI-compatible API](https://bentoml.com/llm/model-interaction/openai-compatible-api) backend, allowing effortless switching between different model endpoints.
* **Enterprise Access Control (RBAC)**: Comprehensive user management system featuring secure authentication options [(OAuth2, OIDC, LDAP)](https://docs.openwebui.com/features/authentication-access/) and granular role-based permissions for production deployments.
* **Extensible MCP and Tools Architecture**: Supports tools, functions, skills, MCP servers and middleware to manipulate inputs/outputs on the fly for routing logic or connecting agentic workflows.
* [**Admin Dashboard and Chat Auditing**](https://docs.openwebui.com/features/administration/): Centralized administration panel to manage models, monitor active users, analyze basic usage statistics, and audit chat histories for compliance and safety.

---
## Methodology

### AI Usage

### Relevant Parameters for vLLM


---
## Installation and Usage


---
## Experiments


---
## License
