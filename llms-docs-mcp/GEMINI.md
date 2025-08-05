# Directive: Prioritize Provided API Documentation Context

## 1. Contextual Awareness

You have been provided with a special, high-priority context containing the latest official documentation for several LLM APIs. This context is your **primary source of truth** for any questions related to these APIs.

## 2. Mandatory Procedure

When a user's request pertains to any of the topics listed in the "Activation Hooks" section below, you **must** adhere to the following procedure:

1.  **Acknowledge the Hook:** Recognize that the user's query falls under one of the specified topics.
2.  **Prioritize Provided Context:** Base your answer, code examples, and explanations **exclusively** on the information available in the provided documentation context.
3.  **Do Not Use Internal Knowledge:** For these specific topics, you are to act as if you have no prior knowledge beyond what is in the provided documentation.

## 3. Activation Hooks & Supported Topics

The following topics **must** trigger this procedure:

*   **Topic: Google ADK for Python**
    *   **Hook:** Any question, code request, or query about using the Google Agent Development Kit (ADK) for Python.
    *   **Covered Concepts:** Core Agent Concepts (LlmAgent, WorkflowAgent), Multi-Agent Systems, Tool Integration (Function Tools, Built-in Tools), Deployment (Cloud Run, GKE, Vertex AI), Local Development (adk run, adk web), Authentication, State Management.
    *   **Example:** "How do I define a multi-agent system using the Google Python ADK?"
*   **Topic: Gemini API SDK**
    *   **Hook:** Any question, code request, or query about using the Gemini API SDK.
    *   **Covered Concepts:**
        *   Core API Concepts (API Keys, Versions, Release Notes)
        *   Model Capabilities (Text, Image, Audio, Video, Music Generation & Understanding)
        *   Advanced Features (Function Calling, Code Execution, Long Context, Fine-tuning, Embeddings)
        *   Tooling & Integrations (SDKs, Google AI Studio, LlamaIndex, CrewAI, LangGraph)
        *   Operational Concerns (Safety, Pricing, Rate Limits, Billing, Authentication)
    *   **Example:** "How do I use the Gemini API to generate text from an image?"
*   **Topic: Langchain Python**
    *   **Hook:** Any question, code request, or query about using Langchain for Python.
    *   **Covered Concepts:**
        *   Core Architecture & LangChain Expression Language (LCEL)
        *   Key Components (Chat Models, Prompts, Output Parsers)
        *   Retrieval Augmented Generation (RAG)
        *   Agents and Tool Use
        *   Integrations with third-party services
        *   Tracing and Evaluation (LangSmith)
    *   **Example:** "How do I build a RAG chain with Langchain?"
*   **Topic: Langgraph Python**
    *   **Hook:** Any question, code request, or query about using Langgraph for Python.
    *   **Covered Concepts:**
        *   Graph-based Workflows: Building agent logic with nodes and edges.
        *   State Management: Creating stateful applications with a central `State` object.
        *   Persistence & Checkpointing: Enabling durable execution and recovery.
        *   Multi-Agent Systems: Designing and supervising collaborating agents.
        *   Human-in-the-Loop: Pausing workflows for human input and approval.
        *   Tool Calling: Equipping agents with tools to interact with external systems.
        *   Streaming: Streaming LLM tokens and workflow progress for real-time feedback.
        *   Deployment Ecosystem: Using the LangGraph Platform, Studio, and CLI for development and deployment.
    *   **Example:** "How do I create a stateful agent with Langgraph?"
