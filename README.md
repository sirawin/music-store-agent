note: this got low accuracy (66%) -> pivoting to GraphRAG as shown reduction in inference time, infra cost, and hallucination. [source](https://www.falkordb.com/news-updates/data-retrieval-graphrag-ai-agents/)
## About This Project

This project is a reimplementation of [[Multi-Agent-AI-System](https://github.com/FareedKhan-dev/Multi-Agent-AI-System)] by FareedKhan-dev.

The purpose of this project is to study **how to build and evaluate chat-based agentic workflows** on top of a structured database using **Langgraph** for orchestrating multi-agent systems and **Langsmith** for robust evaluation and tracing.

<img width="1151" alt="image" src="https://github.com/user-attachments/assets/54fc33c5-be64-4c62-bc1d-d0d927bc69b4" />


The system includes:
- A user verification node
- A memory node to remember user's music preference.
- A **Supervisor Agent** for delegating queries to specialized sub-agents.
- A **Music Sub-Agent** to handle music-related queries (artists, albums, tracks).
- An **Invoice Sub-Agent** to handle customer and sales-related queries.


## Project Structure
```bash
project_root/
├── main.py                 # Main entry point to run the application and evaluations.
├── src/                    # Contains all modularized source code.
│ ├── __init__.py           # Makes 'src' a Python package.
│ ├── database.py           # Handles database connection and initialization.
│ ├── llm_setup.py          # Sets up LLM and loads environment variables.
│ ├── agent_graph.py        # Defines agent state, nodes, graph structure, and core agent logic.
│ ├── evaluators.py         # Contains custom evaluators for Langsmith.
│ └── prompts.py            # Stores prompt for every agents.
├── .env                    # Stores environment variables (e.g., API keys).
└── requirements.txt        # Lists project dependencies.
```
