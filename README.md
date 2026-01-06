# AI Code Generator Agent

An autonomous AI coding agent built with LangChain and Groq that can write, test, and fix Python code automatically.

## Features

- **Autonomous Code Generation**: AI agent that understands requests and generates working code
- **Self-Testing**: Automatically tests generated code and fixes errors
- **Web Search Integration**: Can search for coding solutions and best practices
- **ReAct Framework**: Uses reasoning and action loops for intelligent problem-solving
- **Memory Support**: Maintains conversation context across interactions

## Quick Start

### Prerequisites

- Python 3.8+
- Groq API Key (get it from [console.groq.com](https://console.groq.com))

### Installation

```bash
pip install langchain langchain-groq langchain-community
```

### Setup

1. Get your Groq API key from [console.groq.com](https://console.groq.com)
2. Set it in the notebook

### Usage

```python
# Run the agent with a coding task
response = agent_executor.invoke({
    "input": "Build a simple Python function to calculate factorial"
})
print(response["output"])
```

## How It Works

1. **Understanding**: Agent analyzes your coding request
2. **Planning**: Creates a step-by-step solution plan
3. **Code Generation**: Writes Python code to solve the problem
4. **Testing**: Executes and tests the code using built-in tools
5. **Debugging**: Automatically fixes errors if found
6. **Delivery**: Returns working, tested code

## Available Tools

- `run_code`: Safely execute Python code and return results
- `web_search`: Search for coding help and documentation

## Configuration

The agent uses:

- **Model**: Llama 3.3 70B (via Groq)
- **Temperature**: 0.7 (balanced creativity/consistency)
- **Max Iterations**: 10 (prevents infinite loops)
- **Memory**: Conversation buffer for context retention

## Known Issues

- ReAct output parsing may fail with verbose responses
- Fix: Add `handle_parsing_errors=True` to AgentExecutor

## Acknowledgments

- Built with [LangChain](https://langchain.com/)
- Powered by [Groq](https://groq.com/)
- Uses Llama 3.3 70B model

**Note**: This is an educational project demonstrating agentic AI capabilities. Always review generated code before using in production.
