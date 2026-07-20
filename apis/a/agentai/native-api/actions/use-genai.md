# Use GenAI with Agent.ai

Creates AI-generated text in Agent.ai from instructions.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/invoke_llm`
- **Base URL:** `https://api-lr.agent.ai/v1`
- **Official documentation:** [Use GenAI](https://docs.agent.ai/api-reference/use-ai/use-genai-llm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instructions` | body | `string` | yes | Instructions for the language model. |
| `llm_engine` | body | `string` | yes | LLM model to use for text generation. |
