# Project Kairos

**Kairos** is an autonomous engineering agent designed to bridge the gap between intent and production. It doesn't just plan; it executes. By integrating planning, unit testing, verification, and automated PR generation into a single distributed pipeline, Kairos acts as an extension of the software engineer.

## 🚀 The Agentic Lifecycle
Kairos operates on a closed-loop execution model:
1. **Context-Aware Planning:** Utilizes 3-level Hybrid RAG to map requirements to architectural constraints.
2. **Autonomous Implementation:** Generates production-ready code with integrated test suites.
3. **Verified Execution:** Executes unit tests within the environment, performs diagnostic verification, and self-corrects based on test failures.
4. **Intelligent PR Generation:** Delivers structured Pull Requests with comprehensive impact reports, review summaries, and architectural justifications.

## 🏗️ Architecture
Kairos employs a distributed agentic architecture:
* **Edge Layer (TypeScript MCP):** Secure, local-first context harvesting.
* **Orchestration Layer (Java 21 + Virtual Threads):** Manages the agent's state machine, concurrency, and inter-service communication.
* **Compute Layer (Python):** Executes the specialized ML tasks, re-ranking, and verification logic.
* **IPC Backbone:** Kafka-orchestrated events with Redis-based claim-check context sharing.

## 🛠️ Tech Stack
- **Languages:** Java 21, Python 3.12, TypeScript 6.0
- **Frameworks:** Spring Boot 3.x, FastAPI
- **Databases:** PostgreSQL (pgvector), SQLite (sqlite-vec)
- **Infrastructure:** Kafka, Redis, Ollama

## 🛡️ Design Principles
- **Autonomous Verification:** The agent is not done until the tests pass.
- **Local-First Privacy:** Private code context is vectorized locally before any data leaves the host.
- **Self-Healing Orchestration:** Distributed workflows designed to recover from transient failures automatically.
