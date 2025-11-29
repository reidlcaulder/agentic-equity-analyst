# Agentic Equity Analyst

**Status:** Prototype / Educational Sandbox
**Author:** Reid Caulder

## Overview
Agentic-Equity-Analyst is an autonomous AI system designed to automate the fundamental equity research process.

In traditional finance, a junior analyst spends hours scraping 10-Ks, reading news, and synthesizing risk factors. This project demonstrates how **Agentic AI** can streamline this workflow by deploying a team of specialized agents to perform these tasks in parallel, delivering a comprehensive investment memo in minutes.

## Business Use Case
This tool serves as a proof-of-concept for **GenAI Business Solutions**, specifically:
1.  **Automated Due Diligence:** Rapidly screening stocks for red flags.
2.  **Standardized Reporting:** Ensuring every analysis follows a strict, consistent framework.
3.  **Risk/Reward Synthesis:** Using separate agent roles to force a debate between growth potential and downside risk.

## The Agent Team (CrewAI)
The system orchestrates three specialized agents:

* **The Data Analyst:**
    * *Role:* Quantitative Extraction.
    * *Task:* Extracts key financial ratios, growth metrics, and insider trading activity.
    * *Goal:* Provide a factual data foundation.
* **The Risk Officer:**
    * *Role:* Qualitative Risk Assessment.
    * *Task:* Scans news and filings for regulatory threats, competitor moves, and market headwinds.
    * *Goal:* Identify the "Bear Case" and downside scenarios.
* **The Portfolio Manager:**
    * *Role:* Strategic Synthesis.
    * *Task:* Weighs the Analyst's data against the Risk Officer's warnings to produce a final "Buy/Sell/Hold" recommendation.
    * *Goal:* Produce a decision-ready investment memo.

## Technical Stack
* **Orchestration:** [CrewAI](https://crewai.com) (Agent delegation and process management)
* **Tools:** LangChain (PythonREPL, Web Search)
* **Language:** Python 3.10+
* **LLM Integration:** OpenAI GPT-4o

## Quick Start
1.  Clone the repository.
2.  Install dependencies: `uv sync` or `pip install -r requirements.txt`.
3.  Set your `.env` variables (OPENAI_API_KEY).
4.  Run the analysis:
    ```bash
    python src/stock_picker/main.py
    ```
