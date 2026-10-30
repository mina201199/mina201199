# Hi, I'm Mina Li

AI Application / Software Engineer, moving into AI application development from project management, international trade, and marketing. I build LLM applications whose answers can be checked against their sources, whose queries are guarded before they run, and whose behaviour is pinned down by tests.

- **LLM applications**: Python and FastAPI services that call a local model (Gemma via llama.cpp or Ollama) or the OpenAI API
- **Hybrid retrieval**: BM25 plus embeddings, fused with reciprocal rank fusion (RRF)
- **Citation verification**: citations must map back to a valid source passage; invalid ones are rejected
- **Permission-aware design**: roles, document access, and version checks enforced on the backend, not in the UI
- **Evaluation and testing**: fixed offline benchmarks, pytest, Playwright E2E, and GitHub Actions CI
- **Fine-tuning, judged by evaluation**: LoRA/QLoRA experiments are compared with the current model and not adopted when a key metric regresses
- Background in project management (80+ projects tracked), international trade (20+ overseas clients), and marketing (6 brands): requirements translation and cross-functional coordination

**Portfolio:** <https://mina201199.github.io/resume/> · **Résumé (PDF):** <https://mina201199.github.io/resume/mina-lee-resume.pdf>

## Selected projects

| Project | What it demonstrates | Evidence |
|---|---|---|
| [PredictFix AI Factory](https://github.com/mina201199/predictfix-ai-factory) | A maintenance assistant for CNC factories that joins manual lookup, qualification-based dispatch, supervisor approval, and verified close-out into one traceable workflow (solo project, local MVP) | FastAPI + SQLAlchemy; local Gemma (llama.cpp or Ollama) with manual and case RAG — TF-IDF/BM25 retrieval with optional OpenAI-embedding RRF; backend-verified citations, role permissions, idempotent requests; close-out is blocked until its conditions are met; 161 automated tests ([validation record](https://github.com/mina201199/predictfix-ai-factory/blob/main/docs/release-validation-20261020.md)) and 45/45 AI/API security checks; CI also checks the containers and PostgreSQL. A Gemma QLoRA run raised exact-match accuracy from 18% to 42% but lowered recall, so it was not adopted |
| [PowerQuery TW Text2SQL](https://github.com/mina201199/text2sql_project) | Chinese questions over Taipower open data turned into guarded, read-only SQL; unknown questions are refused or clarified, and OpenAI is optional | Team project, forked from [lee851104/text2sql_project](https://github.com/lee851104/text2sql_project). My part: two PRs merged upstream ([#2](https://github.com/lee851104/text2sql_project/pull/2), [#15](https://github.com/lee851104/text2sql_project/pull/15)), plus the opt-in online evaluation CLI, offline question-coverage expansion, corpus-retrieval fixes, and an admin-credential security fix in the fork. The team built the SQLGlot AST read-only checks, table/column allowlists, and semantic guards; the team's fixed offline benchmark: 60/60 queries, 15/15 SQL attacks blocked, 45/45 semantic traps (rule mode; no online LLM accuracy claimed) |
| [Labor-rights RAG](https://github.com/mina201199/hr-leave-attendance-rag) | Q&A over official Taiwanese labor sources whose answers cite their sources | BM25 + vector hybrid retrieval fused with RRF; citation IDs are verified and the system refuses when the evidence is insufficient; offline source-excerpt mode; [validation report](https://github.com/mina201199/hr-leave-attendance-rag/blob/main/reports/corpus-120-validation-20261021.json) on 18 development checks (not a held-out test set) |
| [Life House](https://github.com/mina201199/life_house) | Team delivery and continued independent development | 3-person team project, Top 10 of 160 teams at a hackathon; walking-distance risk from 230k Taoyuan accident records; [PR #3](https://github.com/lee851104/life_house/pull/3) documents my product, frontend/backend, E2E, and CI contributions |

### Life House — my role

- Built the location A/B comparison, share links and local favorites; also contributed FastAPI/frontend changes, Playwright E2E tests, and CI test-data flow.
- For the [competition demo video](https://youtu.be/3uHAfHad2d0), I created the opening AI-generated sequence and re-edited the final video. The later AI-generated segment was made by a teammate using Claude.

### More projects

- **[Secure Multi-Tenant RAG](https://github.com/mina201199/secure-multi-tenant-rag)** — A multi-company document platform with company- and role-scoped access, document versioning, share/revoke, and audited transfers on FastAPI, PostgreSQL, and Docker; row-level security and the RAG layer are still in progress.
- **[Amazon 571M Candidate Retrieval](https://github.com/mina201199/amazon-recsys-571m)** — A single-machine pipeline over 571M Amazon review interactions with five recall channels, weighted RRF, and time-split offline evaluation.
- **[SECOM Cost-Sensitive Evaluation](https://github.com/mina201199/secom-cost-sensitive-eval)** — Tests whether a defect model is worth deploying: 18 model × policy × capacity configurations under walk-forward backtesting, none of which beat the model-free inspection policies.

## Training

- **AI Large Language Model (LLM) Engineer Program** (486 hours), 資展國際 / Institute for Information Industry (III), 2026/06 – 2026/11 — RAG, Text-to-SQL, LoRA/QLoRA fine-tuning, and FastAPI AI services; team project work with Git branches, pull-request review, and CI.

## Core stack

`Python` `SQL` `FastAPI` `Pydantic` `SQLAlchemy` `Alembic` `SQLite` `PostgreSQL` `pgvector` `Docker` `Docker Compose` `SQLGlot` `OpenAI API` `llama.cpp` `Ollama` `LoRA/QLoRA` `pandas` `DuckDB` `Parquet` `scikit-learn` `LightGBM` `Streamlit` `pytest` `Playwright` `GitHub Actions` `Tailscale Funnel`

I care about traceable answers, honest baselines, explicit failure modes, and saying clearly what a project has not done yet.
