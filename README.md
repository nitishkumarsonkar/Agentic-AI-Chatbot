# LangGraph Multi-Tool Chatbot

A Python-based chatbot implementation using LangGraph that combines multiple information retrieval tools including Arxiv, Wikipedia, and Tavily search capabilities. The chatbot uses a sophisticated workflow to process queries and provide comprehensive responses.

## Features

- Multiple information sources integration:
  - Arxiv papers search
  - Wikipedia queries
  - Tavily web search
- LangChain integration with Groq LLM
- State management using LangGraph
- Interactive conversation flow
- Customizable tool configurations

## Prerequisites

- Python 3.13.4 or higher
- Virtual environment (recommended)

## Dependencies

```
pydantic
langchain
langchain-core
langchain-community
python-dotenv
langchain-groq
arxiv
wikipedia
langgraph
```

## Setup

1. Create a virtual environment:
```bash
python3 -m venv venv
source venv/bin/activate
```

2. Install the required packages:
```bash
pip install -r requirements.txt
```

3. Create a `.env` file with the following API keys:
```
TAVILY_API_KEY=your_tavily_api_key
GROQ_API_KEY=your_groq_api_key
```

## Project Structure

- `chatbotmultipletools.ipynb`: Main Jupyter notebook containing the chatbot implementation
- `requirements.txt`: List of Python package dependencies
- `.env`: Environment variables for API keys (not tracked in git)

## Features Implementation

The chatbot implements the following key components:

1. Tool Integration:
   - Arxiv search with customizable result limits
   - Wikipedia queries with content length control
   - Tavily search for real-time web information

2. LLM Configuration:
   - Uses Groq's qwen-qwq-32b model
   - Configured with temperature=0.1 for consistent responses
   - Maximum token limit of 1000

3. Graph-based Workflow:
   - State management for conversation context
   - Conditional tool selection based on query type
   - Recursive processing for complex queries

## Usage

Open the Jupyter notebook `chatbotmultipletools.ipynb` and run the cells sequentially. The chatbot can handle various types of queries including:

- Academic paper searches
- Wikipedia information retrieval
- Current events and news
- Combined queries across multiple sources

## Example Queries

- Research paper lookups: "What is the latest research on quantum computing?"
- General knowledge: "What is machine learning?"
- Current events: "What are the recent AI developments?"
- Multi-tool queries: "Tell me about recent AI news and quantum computing research"