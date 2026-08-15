# Fayna Digital

Engineering agency building operational infrastructure for EU manufacturing, e-commerce, and tourism businesses — connecting shopfloors, ERP systems, and AI workflows.

---

### What We Do

- **ERP & Core Business Systems**
  We implement, extend, and maintain Odoo (v17–v19) platforms aligned with actual operational processes. We develop custom modules, resolve migration bottlenecks, and implement regulatory compliance integrations, including Poland's KSeF 2.0 electronic invoicing.

- **Industrial IoT & Shopfloor Execution**
  We connect shopfloor machinery directly to management systems. Utilizing Modbus TCP bridges and dedicated operator kiosks, we capture production metrics and synchronize work center statuses with Odoo MRP in real time.

- **AI Infrastructure & Retrieval Systems**
  We build deterministic AI pipelines, custom Model Context Protocol (MCP) servers, and local RAG architectures on FAISS. We orchestrate specialized models via OpenRouter (DeepSeek, Gemini, Qwen, Moonshot/Kimi, GLM) and run local ASR (faster-whisper) for internal knowledge access and workflow automation.

- **Enterprise Integrations & Telephony**
  We bridge external communication and marketing services into central CRM and ERP workflows, integrating VoIP telephony (Zadarma), automated chat channels (SendPulse), and server-side tracking (Meta CAPI).

---

### Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Odoo](https://img.shields.io/badge/Odoo_17_|_18_|_19-714B67?style=for-the-badge&logo=odoo&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Modbus TCP](https://img.shields.io/badge/Modbus_TCP-00599C?style=for-the-badge)
![FAISS](https://img.shields.io/badge/FAISS_RAG-000000?style=for-the-badge)
![OpenRouter](https://img.shields.io/badge/OpenRouter_API-6366F1?style=for-the-badge)

---

### Selected Open-Source Repositories

| Repository | Purpose | Stack |
| :--- | :--- | :--- |
| [`local-rag-mcp`](https://github.com/fayna-digital/local-rag-mcp) | Local knowledge base MCP server for structured context retrieval in LLM pipelines. | Python, FAISS, MCP |
| [`l10n-pl-ksef-margin`](https://github.com/fayna-digital/l10n-pl-ksef-margin) | Polish KSeF 2.0 e-invoicing compliance and VAT margin procedure engine for Odoo. | Odoo, Python, XML |
| [`demo-industrial-iot`](https://github.com/fayna-digital/demo-industrial-iot) | Telemetry bridge reading PLC data to update work orders in Odoo MRP automatically. | Python, Modbus TCP, Odoo |
| [`shopfloor-kiosk`](https://github.com/fayna-digital/shopfloor-kiosk) | Operator touch interface and monitoring dashboard for manufacturing lines. | Python, Linux, Docker |
| [`zadarma-odoo`](https://github.com/fayna-digital/zadarma-odoo) | PBX telephony integration for Odoo CRM: click-to-call, call logging, and recording sync. | Odoo, REST API, Python |

---

### Engineering Method

We approach software delivery through structured technical discipline:

1. **Specification Before Code**: Requirements, data schemas, and edge cases are fully defined prior to execution.
2. **Model Orchestration**: Workflows use multi-model pipelines routed through OpenRouter, matching specific models to extraction, transformation, or reasoning tasks.
3. **Mechanical Verification**: Pipelines enforce automated linting, type checks, and schema validation at every boundary.
4. **Live Execution Testing**: Systems are validated through end-to-end runtime runs against actual target states rather than theoretical unit assertions alone.

---

### Contact

- **Website**: [fayna.agency](https://fayna.agency)
- **CTO**: Volodymyr Shevchenko · [GitHub](https://github.com/VladSh77) · [LinkedIn](https://www.linkedin.com/in/vladshua)
- **Base**: Poland
