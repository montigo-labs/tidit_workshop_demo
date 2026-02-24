# All Agentic Architectures

Welcome to a comprehensive, hands-on masterclass in **modern AI agent design**. This repository contains detailed implementations of **5 state-of-the-art agentic architectures**, built with LangChain and LangGraph. It is designed to be a living textbook, bridging the gap between theoretical concepts and practical, production-ready code. The original repo https://github.com/FareedKhan-dev/all-agentic-architectures/blob/main/03_ReAct.ipynb has been adapted for the demo in the TIDIT AI Workshop on Agentic AI. 

## 📖 Why This Repository?

The field of AI agents is evolving at an incredible pace, but many resources remain abstract and theoretical. This project was created to provide a structured, practical, and deeply educational path for developers, researchers, and AI enthusiasts to master the art of building intelligent systems.

-   **From Theory to Tangible Code:** Each architecture is not just explained but implemented end-to-end in a runnable Jupyter notebook.
-   **Structured Learning Path:** The notebooks are ordered to build concepts progressively, from foundational patterns to highly advanced, multi-agent and self-aware systems.
-   **Emphasis on Evaluation:** We don't just build agents, we measure them. Most notebooks feature a robust `LLM-as-a-Judge` pattern to provide quantitative, objective feedback on an agent's performance, a critical skill for production AI.
-   **Real-World Scenarios:** The examples are grounded in practical applications—financial analysis, coding, social media management, medical triage—making the concepts immediately relevant.
-   **Consistent, Modern Framework:** By using `LangGraph` as the core orchestrator, you will learn a powerful, stateful, and cyclical approach to agent design that is rapidly becoming the industry standard.

---

## 🏛️ The Architectures: A Deep Dive

This collection covers the full spectrum of modern agentic design, from single-agent enhancements to complex, collaborative, and self-improving systems.

| # | Architecture | Core Concept / TL;DR | Key Use Case | Notebook |
|:---:|---|---|---|:---:|
| **01** | **Reflection** | Moves from a single-pass generator to a deliberate, multi-step reasoner by critiquing and refining its own work. | High-Quality Code Generation, Complex Summarization | [01_reflection.ipynb](./01_reflection.ipynb) |
| **02** | **Tool Use** | Empowers an agent to overcome knowledge cutoffs and interact with the real world by calling external APIs and functions. | Real-time Research Assistants, Enterprise Bots | [02_tool_use.ipynb](./02_tool_use.ipynb) |
| **03** | **ReAct** | Dynamically interleaves reasoning ("thought") and action ("tool use") in an adaptive loop to solve complex, multi-step problems. | Multi-hop Q&A, Web Navigation & Research | [03_ReAct.ipynb](./03_ReAct.ipynb) |
| **04** | **Planning** | Proactively decomposes a complex task into a detailed, step-by-step plan *before* execution, ensuring a structured and traceable workflow. | Predictable Report Generation, Project Management | [04_planning.ipynb](./04_planning.ipynb) |
| **05** | **Multi-Agent Systems** | A team of specialized agents collaborates to solve a problem, dividing labor to achieve superior depth, quality, and structure in the final output. | Software Dev Pipelines, Creative Brainstorming | [05_multi_agent.ipynb](./05_multi_agent.ipynb) |

---

## 🚀 Getting Started

Follow these steps to set up your local environment and run the notebooks.

### 1. Clone the Repository

```bash
git clone https://github.com/montigo-labs/tidit_workshop_demo
cd all-agentic-architectures
```

### 2. Set Up a Virtual Environment

It is highly recommended to use a virtual environment to manage dependencies.

```bash
# For Unix/macOS
python3 -m venv venv
source venv/bin/activate

# For Windows
python -m venv venv
.\venv\Scripts\activate
```

### 3. Install Dependencies

Install all the required Python packages from the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

The agents require API keys to function. Create a file named `.env` in the root of the project directory. You can copy the provided `requirements.txt` content to see what's needed and then create your `.env` file.

Open the `.env` file and add your credentials. It should look like this:

```python
# .env file

# Nebius AI API Key (for LLM access)
TOGETHER_API_KEY="your_nebius_api_key_here"

# LangSmith API Key (for tracing and debugging)
LANGSMITH_API_KEY="your_langsmith_api_key_here"
LANGSMITH_TRACING="true"
LANGSMITH_PROJECT="TIDIT_Workshop" # Optional: Set a project name

# Tavily Search API Key (for the Research agent's tool)
TAVILY_API_KEY="your_tavily_api_key_here"
```

### 5. Run the Notebooks

You can now launch Jupyter and explore the notebooks in numerical order.

```bash
jupyter notebook
```