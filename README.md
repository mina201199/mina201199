# Hi, I'm Mina Lee

AI Application / Software Engineer. I build LLM applications whose answers can be checked against their sources, whose queries are guarded before they run, and whose behaviour is pinned down by tests.

- **LLM applications**: Python and FastAPI services that call a local model (llama.cpp or Ollama) or the OpenAI API
- **Hybrid retrieval**: BM25 plus embeddings, fused with reciprocal rank fusion (RRF)
- **Citation verification**: citations must map back to a valid source passage; invalid ones are rejected
- **Permission-aware design**: roles, document access, and version checks enforced on the backend, not in the UI
- **Evaluation and testing**: fixed offline benchmarks, pytest, Playwright E2E, and GitHub Actions CI
- Project-management background: requirements translation, cross-functional coordination, and delivery tracking across 80+ projects

**Portfolio:** <https://mina201199.github.io/resum/> · **Résumé (PDF):** <https://mina201199.github.io/resum/mina-lee-resume.pdf>

## Selected projects

| Project | What it demonstrates | Evidence |
|---|---|---|
| [PredictFix AI Factory](https://github.com/mina201199/predictfix-ai-factory) | A maintenance copilot for CNC factories that joins manual lookup, qualification-based dispatch, and verified close-out into one traceable workflow (local MVP) | FastAPI + SQLAlchemy; TF-IDF/BM25 retrieval with optional OpenAI-embedding RRF; local LLM via llama.cpp or Ollama; citation verification, role permissions, idempotent requests; 161 automated tests ([validation record](https://github.com/mina201199/predictfix-ai-factory/blob/main/docs/release-validation-20261020.md)); CI also checks the containers and PostgreSQL |
| [PowerQuery TW Text2SQL](https://github.com/mina201199/text2sql_project) | Chinese questions over Taipower open data turned into guarded, read-only SQL | Team project, forked from [lee851104/text2sql_project](https://github.com/lee851104/text2sql_project); my part is the opt-in online evaluation CLI and the offline question-coverage expansion. SQLGlot AST read-only checks, table/column allowlists, and semantic guards; fixed offline benchmark: 60/60 queries, 15/15 SQL attacks blocked, 45/45 semantic traps (rule mode; no online LLM accuracy claimed) |
| [Life House](https://github.com/mina201199/life_house) | Team delivery and continued independent development | Team project, Top 10 of 160 teams; [PR #3](https://github.com/lee851104/life_house/pull/3) documents my product, frontend/backend, E2E, and CI contributions |

### Life House — my role

- Built the location A/B comparison, share links and local favorites; also contributed FastAPI/frontend changes, Playwright E2E tests, and CI test-data flow.
- For the [competition demo video](https://youtu.be/3uHAfHad2d0), I created the opening AI-generated sequence and re-edited the final video. The later AI-generated segment was made by a teammate using Claude.

### More projects (private — demo available on request)

- **Labor-rights RAG** — Q&A over Taiwanese labor-rights sources and labor-penalty records, using BM25 + embedding hybrid retrieval with RRF, citation checks, and refusal when the evidence is insufficient.
- **Secure Multi-Tenant RAG** — A multi-company document platform with company- and role-scoped access, document versioning, share/revoke, and audited transfers on FastAPI, PostgreSQL, and Docker; row-level security and the RAG layer are still in progress.
- **Amazon 571M Candidate Retrieval** — A single-machine pipeline over 571M Amazon review interactions with five recall channels, weighted RRF, and time-split offline evaluation.
- **SECOM Cost-Sensitive Evaluation** — Tests whether a defect model is worth deploying: 18 model × policy × capacity configurations under walk-forward backtesting, none of which beat the model-free inspection policies.

## Core stack

`Python` `SQL` `FastAPI` `SQLAlchemy` `SQLite` `PostgreSQL` `Docker` `SQLGlot` `OpenAI API` `llama.cpp` `Ollama` `pandas` `DuckDB` `Parquet` `scikit-learn` `LightGBM` `Streamlit` `pytest` `Playwright` `GitHub Actions`

I care about traceable answers, honest baselines, explicit failure modes, and saying clearly what a project has not done yet.
