
# Multi-Agent Collaboration Framework

# Overview

This project demonstrates a multi-agent collaboration framework where different specialized agents work together under the supervision of a central supervisor agent to perform complex tasks. The agents include:

Researcher: Handles research tasks using a search tool.

Coder: Executes and generates code for programming tasks.

Chart Generator: Creates visualizations such as graphs based on data.

The supervisor agent coordinates the workflow, ensuring tasks are routed to the appropriate agents and executed sequentially or collaboratively as required.

# Features

Dynamic Task Routing: The supervisor decides which agent acts next based on the task's state.

Specialized Agents: Each agent is tailored for specific functionalities:

Researcher: Conducts online searches using the Tavily search tool.

Coder: Executes and generates Python code securely.

Chart Generator: Creates graphical visualizations.

State Management: Maintains a structured workflow graph with state transitions.

Extensibility: Easily add more agents or modify the workflow as needed.

# Setup Instructions

Prerequisites

Python 3.8 or higher

Install required libraries:

pip install -U langgraph langchain langchain_openai langchain_experimental langsmith pandas

API keys for the following:

OpenAI: For language model functionality

LangChain: For managing and tracing interactions

Tavily: For search capabilities

# Environment Variables

Set the following environment variables for API access:

OPENAI_API_KEY

LANGCHAIN_API_KEY

TAVILY_API_KEY

# How It Works

Workflow

Supervisor Initialization: The supervisor agent initializes the workflow and assigns tasks to agents.

Agent Execution: Each agent performs its task and returns results to the supervisor.

Result Aggregation: The supervisor collects results and determines the next action or terminates the workflow.
