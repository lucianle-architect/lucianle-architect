```markdown
# Lucian Le

### Systems Architect & Full-Stack Builder
**Architecting OMNIA - Local-First, Zero-Marginal-Cost Multi-Agent AI Infrastructure**

`Hanoi, Vietnam` | `Local-First LAN Mesh` | `MCP / JSON-RPC 2.0` | `OMNIA v2.x`

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

```

### Core Capabilities

* **Multi-Agent Coordination:** Routes tasks across local Ollama models and external AI agents with runtime concurrency controls, approval gates, and self-healing pipeline loops.
* **Deterministic State & Context:** Uses SQLite WAL mode with FTS5 full-text and vector hybrid search, ETag-cached context injection (`/api/t5t/context`), and automated `VACUUM` + WAL checkpoints.
* **Workstation & Visual Extensions:** Integrates Windows background orchestration via PowerShell, global hotkeys, **T5T** daily/weekly rollups, and `media_studio` procedural GLSL shader rendering (`moderngl`, Raymarching SDF, Curl Noise, Cymatics).

---

## Tech Stack

| Layer | Technologies |
| --- | --- |
| **AI & Agent Orchestration** | `Ollama`, `MCP (JSON-RPC 2.0)`, `Gemini`, `Claude`, `Codex`, `nomic-embed-text` |
| **Backend & Systems** | `Python` (`Flask`, `pytest`), `PHP` (`Laravel`, `Eloquent`, `JWT`), `Node.js` (`Express`), `PowerShell` |
| **Data & Storage** | `SQLite` (`WAL`, `FTS5`), Hybrid Vector Search, `Supabase` |
| **Frontend & UI** | `React`, `Next.js`, `TypeScript`, `Tailwind CSS`, `HTML5 / CSS3`, `Bootstrap` |
| **Creative & Visualization** | `moderngl`, `GLSL Shaders` (Raymarching SDF, Curl Noise, Cymatics) |
| **Infrastructure & Tooling** | `Git`, `Docker`, `Cloudflare Tunnels`, `Slack Webhooks`, `Figma`, `StarUML` |

---

## Connect

* **GitHub:** `@lucianle-architect`
* **LinkedIn:** `lucianle-architect`
* **Email:** `lucianle.architect@gmail.com`

```

<ElicitationsGroup message="File README.md đã nằm gọn trên DESKTOP-D9EMEKK, bạn muốn đẩy lên GitHub ngay không?">
  <Elicitation label="Khởi tạo & push Profile README" query="Hãy khởi tạo git repo tại C:\Users\ADMIN\Documents\GitHub\lucianle-architect và push file README.md lên GitHub qua SSH."/>
  <Elicitation label="Tạo repo cho OMNIA Control Center" query="Hãy hướng dẫn tôi tạo repository cho dự án OMNIA và cấu hình .gitignore chuẩn cho Python, Node.js và SQLite WAL."/>
  <Elicitation label="Hoàn thiện hồ sơ LinkedIn" query="Hãy viết lại phần Headline, About và Experience chuẩn tiếng Anh cho Lucian Le để dán lên LinkedIn."/>
</ElicitationsGroup>

```
