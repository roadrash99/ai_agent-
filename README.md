# Research Assistant Agent

This project demonstrates how to build an AI-powered research assistant using [LangGraph](https://github.com/langchain-ai/langgraph) and [Groq](https://groq.com/). The assistant can answer research queries by leveraging multiple tools, including Arxiv, Wikipedia, and Tavily Search.

## Features

- **Multi-tool Integration**: Query Arxiv papers, Wikipedia articles, and perform web searches.
- **Conversational AI**: Uses Groq's large language models for natural language understanding and response generation.
- **Modular Graph Architecture**: Built with LangGraph for flexible and extensible workflow management.

## Requirements

- Python 3.8+
- [langchain_community](https://github.com/langchain-ai/langchain)
- [langgraph](https://github.com/langchain-ai/langgraph)
- [langchain_groq](https://github.com/langchain-ai/langchain-groq)
- [python-dotenv](https://pypi.org/project/python-dotenv/)
- API keys for Groq and Tavily

## Setup

1. **Clone the repository** and navigate to the project directory.

2. **Install dependencies**:
    ```bash
    pip install langchain_community langgraph langchain_groq python-dotenv
    ```

3. **Set up environment variables**:

    Create a `.env` file in the project root with your API keys:
    ```
    GROQ_API_KEY=your_groq_api_key
    TAVILY_API_KEY=your_tavily_api_key
    ```

4. **Run the Jupyter Notebook**:

    Open `chatbotmultipletools.ipynb` in Jupyter and run all cells to initialize the research assistant.

## Usage

- Enter your research question in the notebook interface.
- The assistant will use the most relevant tool (Arxiv, Wikipedia, or Tavily Search) to find and summarize information.
- Responses are generated using Groq's LLM for high-quality, context-aware answers.

## Example

```python
# Example usage in the notebook:
response = graph.invoke({"messages": [{"role": "user", "content": "What are the latest advancements in quantum computing?"}]})
print(response)