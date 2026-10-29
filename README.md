# Conversational AI Chatbot

A conversational AI project built with Python, LangChain, LangGraph, and OpenAI. This project explores LLM integration, conversation memory, streaming responses, and graph-based workflow orchestration through two Jupyter notebooks.

## Overview

The repository contains two notebooks that demonstrate the progression from a basic LLM application to a more structured conversational chatbot.

## Features

- **LLM Integration:** Uses OpenAI's GPT-4o-mini through LangChain.
- **Conversation Memory:** Maintains conversational context across multiple turns.
- **Graph-Based Workflow:** Uses LangGraph to organize chatbot execution.
- **Streaming Responses:** Streams model output as it is generated.
- **Conversation History Management:** Trims message history to help manage token limits.
- **Configurable System Prompt:** Supports customization of the chatbot's instructions, including language preferences.
- **Session Management:** Uses thread-based identifiers to maintain separate conversation states.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| LangChain | LLM integration and message handling |
| LangGraph | Workflow orchestration and state management |
| OpenAI GPT-4o-mini | Language model |
| MemorySaver | Conversation state persistence |
| Jupyter Notebook | Development and experimentation |

## Project Structure

```text
Conversational-Ai-Chatbot/
│
├── conversational_ai_chatbot.ipynb
├── simple_llm_application.ipynb
└── README.md
```

### Notebooks

**1. `conversational_ai_chatbot.ipynb`**

The main project notebook, demonstrating a conversational chatbot with LangGraph orchestration, conversation memory, streaming output, configurable prompts, and message-history management.

**2. `simple_llm_application.ipynb`**

A foundational notebook demonstrating basic LLM setup and integration with LangChain. It provides background for understanding the model initialization used in the main chatbot project.

## How It Works

1. The user submits a message.
2. The chatbot processes the conversation through its LangGraph workflow.
3. The model generates a response using the available conversation context.
4. Conversation state is maintained using thread-based sessions and `MemorySaver`.
5. The response is streamed to the user.
6. Message history is managed to help keep the conversation within token limits.

## Key Concepts Demonstrated

- Large Language Models (LLMs)
- LangChain model integration
- LangGraph workflows
- Stateful conversational applications
- Conversation memory and session management
- Streaming LLM responses
- Message-history management
- Prompt configuration
- API key management

## Future Improvements

- Add automated evaluation of response quality.
- Implement more robust error handling and retry logic.
- Add a user interface beyond Jupyter Notebook.
- Introduce conversation logging and observability.
- Explore additional models and workflow capabilities.

## Installation and Setup

### Prerequisites

- Python 3.10 or later
- Jupyter Notebook
- An OpenAI API key

### 1. Clone the Repository

```bash
git clone https://github.com/nofelmahmoodsubhani/Conversational-Ai-Chatbot.git
cd Conversational-Ai-Chatbot
```

### 2. Install Dependencies

```bash
pip install langchain langchain-openai langgraph jupyter typing_extensions
```

### 3. Configure Your API Key

Set your OpenAI API key as an environment variable.

**Windows PowerShell:**

```powershell
$env:OPENAI_API_KEY="your_api_key_here"
```

**macOS/Linux:**

```bash
export OPENAI_API_KEY="your_api_key_here"
```

Replace `your_api_key_here` with your actual API key. Never commit API keys or other secrets to GitHub.

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `conversational_ai_chatbot.ipynb` to explore and run the main chatbot notebook.

**Note:** These notebooks are intended for learning and experimentation. Run the cells in order and ensure your API key and required dependencies are configured before execution.
