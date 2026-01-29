### FarmVital-AI0
## FarmVital AI - Intelligent Pest & Disease Risk Assessment System

FarmVital AI is a LangFlow-based AI agent for proactive crop health monitoring. It analyzes environmental data (temperature, humidity, rainfall) and crop details to detect pest/disease risks using RAG on IPM guidelines, powered by IBM Granite models via watsonx.ai.
​
## Key Features
  * Unified agent handles data analysis, risk detection, and non-chemical advisories.
  
  * 3 modes: Casual chat, general advice (no numbers), precise numerical assessments.
  
  * RAG vector store with Astra DB for accurate, guideline-based insights.
  
  * Web search integration for real-time updates.

## Tech Stack
* Platform: LangFlow (v1.7.1).

* LLM/Embeddings: IBM watsonx.ai (Granite models, e.g., ibm/granite-3-8b-instruct).

* Vector Store: Astra DB (collection: testdb0, database: maindb0).​

*  Tools: Agent with web search, current date tool.

## Quick Setup
* Install LangFlow: pip install langflow.

* Get credentials:

    * IBM watsonx.ai: API key, project ID, endpoint (e.g., https://jp-tok.ml.cloud.ibm.com).

    * Astra DB: Application token, database ID.

* Ingest IPM/agricultural docs into Astra DB vector store via the flow's ingest node.

## How to Use
  * Import Flow: Open LangFlow, import FarmVital-AI0.json.

  * Configure Components:

    * Watsonx Embeddings/LLM: Enter API key, project ID, select models (e.g., ibm/granite-embedding-278m-multilingual).​

    * Astra DB: Token, collection (testdb0), database (maindb0), keyspace (default_keyspace).

* Agent: Paste system prompt (polite, 3-mode instructions from prior chat).

* Ingest Data: Load PDF/text files of IPM guidelines/extension resources into "Ingest Data" node.

## Run Flow:
* Chat input: Enter query (e.g., "Tomato, 32°C, 85% humidity").

* Output: Point-wise risk summary, alerts, tips.
