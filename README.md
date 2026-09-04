# Research Workspace

Research Workspace is an agent-ready research instrument builder. The core workflow is **Idea -> Research Question -> Questionnaire -> Publish -> Responses**.

## Architecture

- React + Vite frontend
- AppDeploy backend APIs and persistence
- Provider-neutral AI gateway with OpenAI, Anthropic and Gemini adapters
- Encrypted user-provided AI credentials
- Public anonymous questionnaire/respondent flow
- MCP endpoint at `/mcp` for agent access

## Important product rule

Creating research does not pre-populate a questionnaire. A researcher first records an idea, establishes a research question, and then receives an intentionally empty questionnaire. AI can propose or critique questions, but does not silently add them.

## Local/deployment note

This repository contains the AppDeploy implementation. AppDeploy SDK credentials, database, authentication, and deployment configuration are supplied by the target deployment environment. Never commit API keys or encryption secrets.

## MCP

The current implementation exposes research tools through a bearer-token protected MCP HTTP endpoint. OAuth-based MCP authorization can be hardened as a subsequent infrastructure phase.
