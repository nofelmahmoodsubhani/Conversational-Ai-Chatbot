# Conversational AI Chatbot with LangGraph

A conversational AI chatbot built using LangChain, LangGraph, and OpenAI GPT-4o-mini. This project explores how to maintain conversation history, manage context length, generate responses in different languages, and stream AI output.

## Features

- **Conversational Memory:** Maintains conversation state across multiple turns using LangGraph's `MemorySaver`.
- **Session Management:** Uses thread IDs to distinguish conversation sessions.
- **Multilingual Responses:** Uses a configurable system prompt to generate responses in the requested language.
- **Context Management:** Trims conversation history to a defined token limit to manage context length.
- **Streaming Responses:** Displays AI output incrementally rather than waiting for the entire response.
- **Graph-Based Workflow:** Uses LangGraph's `StateGraph` to organize and execute the chatbot workflow.

## Tech Stack

- Python
- LangChain
- LangGraph
- OpenAI GPT-4o-mini
- Jupyter Notebook

## How It Works

1. The user submits a message along with the preferred response language.
2. LangGraph receives the input and passes the conversation state to the model node.
3. The conversation history is trimmed according to the configured token limit.
4. LangChain formats the system prompt and conversation messages.
5. OpenAI GPT-4o-mini generates a response in the requested language.
6. LangGraph maintains conversation state through `MemorySaver` and supports streamed output.

## Concepts Demonstrated

This project demonstrates practical implementations of:

- Stateful conversational AI
- Message persistence and session tracking
- Custom graph state schemas
- Prompt templates and message placeholders
- Conversation-history trimming
- Streaming model responses
- LangGraph workflow construction

## Project Structure

```text
.
└── chatbot.ipynb
```

## Project Scope

This repository contains a Jupyter notebook demonstrating conversational AI concepts and their implementation. It is an experimental learning project rather than a standalone, production-ready chatbot application.

## Future Improvements

- Build an interactive chat interface.
- Add persistent storage beyond in-memory conversation checkpoints.
- Improve context management and conversation summarization.
- Add error handling and configuration management.
- Introduce automated tests for conversation memory and response behavior.

## Installation and Setup

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd <your-repository-folder>
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it:

**Windows**
```bash
.venv\Scripts\activate
```

**macOS/Linux**
```bash
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install langchain langchain-openai langgraph jupyter typing_extensions
```

### 4. Configure the OpenAI API Key

The notebook prompts for your API key if `OPENAI_API_KEY` is not already set.

Alternatively, set the environment variable before launching Jupyter.

**Windows PowerShell**
```powershell
$env:OPENAI_API_KEY="your-api-key"
```

**macOS/Linux**
```bash
export OPENAI_API_KEY="your-api-key"
```

### 5. Run the Notebook

Launch Jupyter:

```bash
jupyter notebook
```

Open `chatbot.ipynb` and execute the cells in order.
