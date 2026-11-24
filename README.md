<div align="center">

# Lucian Le

### Systems Architect & Full-Stack Builder
**Architecting OMNIA — Local-First, Zero-Marginal-Cost Multi-Agent AI Infrastructure**

[![Location](https://img.shields.io/badge/Location-Hanoi%2C%20Vietnam-0f172a?style=flat-square)](#)
[![Architecture](https://img.shields.io/badge/Architecture-Local--First%20LAN%20Mesh-0284c7?style=flat-square)](#omnia-architecture)
[![Protocol](https://img.shields.io/badge/Protocol-MCP%20%2F%20JSON--RPC%202.0-10b981?style=flat-square)](#omnia-architecture)
[![Status](https://img.shields.io/badge/OMNIA%20v2.x-Active%20Build-f59e0b?style=flat-square)](#omnia-architecture)

</div>

---

## About & Engineering Philosophy

I build **open, extensible, and local-first software systems** that remain under developer control without recurring API lock-in. Rather than treating AI agents as isolated chat windows, I design coordinated runtime topologies where local models and frontier agents share persistent state, task queues, and automated verification loops.

* **Dual-Node LAN Orchestration:** Linking `DESKTOP-D9EMEKK` and `AsusVivobook15` over a local mesh to share execution pipelines, background workers, and state endpoints.
* **Zero-Marginal-Cost & Hybrid Retrieval:** Pairing local **Ollama** inference and `nomic-embed-text` embeddings with **SQLite (WAL + FTS5)** persistence (`omnia.db`, `queue.db`, `handoffs.db`) and frontier agents (`Gemini`, `Claude`, `Codex`) when needed.
* **Open-Ended Extensibility:** Grounded in a charter-driven core (**AETHEL HEART**) with hot-pluggable modules (`aethel_heart`, `media_studio`), automated health/WAL maintenance, and daily **T5T** (`2 signals, 2 bottlenecks, 1 delta`) calibration loops.

---

## OMNIA Architecture

```text
+-----------------------------------------------------------------------+
|                     OMNIA CONTROL CENTER & CONSOLE                    |
|        Web Console (:3000) | System Tray (Ctrl+Alt+O / Ctrl+Alt+T)    |
+-----------------------------------+-----------------------------------+
                                    |
        +---------------------------+---------------------------+
        v                                                       v
+-------------------------------+               +-------------------------------+
|     MULTI-AGENT ROUTING &     |               |     PERSISTENCE & MEMORY      |
|       EXECUTION LAYER         |               |          SUBSYSTEM            |
|                               |               |                               |
|  * Smart Auto-Router & Cron   |               |  * SQLite WAL + FTS5          |
|  * MCP Server (JSON-RPC 2.0)  |               |  * nomic-embed-text Hybrid    |
|  * Gemini / Claude / Codex    |               |  * omnia.db / queue.db /      |
|  * Local Ollama (:11434)      |               |    handoffs.db                |
+---------------+---------------+               +---------------+---------------+
                |                                               |
                +-----------------------+-----------------------+
                                        |
                                        v
+-----------------------------------------------------------------------+
|                   LAN MESH, PLUGINS & EDGE EXPOSURE                   |
|  Dual-PC Mesh (DESKTOP-D9EMEKK <-> AsusVivobook15) | Ports 8765/8766 |
|  PowerShell Orchestrator (omnia-stack.ps1) | Cloudflare Named Tunnels |
|  Plugins: Aethel Heart & Media Studio (GLSL / Raymarching / Audio)    |
+-----------------------------------------------------------------------+
