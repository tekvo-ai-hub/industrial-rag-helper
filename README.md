# Maintenance Knowledgebase Assistant

**Industry:** Manufacturing

**Repository:** [tekvo-ai-hub/industrial-rag-helper](https://github.com/tekvo-ai-hub/industrial-rag-helper)

## Description
Local RAG system for machine error diagnostics using manuals and logs.

## Requirements
### Functional
- Ingest equipment manuals.
- Answer queries about machine faults.
- Provide resolution steps from logs.
### Non-Functional
- Offline/Edge capable.
- High recall in retrieval.
- Easy upload interface.
## Solution Design
**LLM:** Mixtral (LoRA fine-tuned)
**Vector DB:** Milvus

### Components
- Log Ingestor
- PDF Manual Parser
- RAG Engine
- Answer Validator
### Data Flow
$ Logs → Clean → Chunk → Embed → Retrieve → Prompt → LLM → Response

### Tech Stack
- **Frontend:** Tauri (Desktop App)
- **Backend:** Rust + Python
- **Storage:** Local
- **Deployment:** Standalone App
