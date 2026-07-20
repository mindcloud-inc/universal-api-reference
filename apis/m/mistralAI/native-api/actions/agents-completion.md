# Agents Completion with Mistral AI

Creates an agent completion in Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/agents/completions`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Agents Completion](https://docs.mistral.ai/api/endpoint/agents#operation-agents_completion_v1_agents_completions_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | yes | The ID of the agent to use for this completion. |
| `messages[]` | body | `array<object>` | yes | Prompt messages encoded as a list of role/content objects. |
| `max_tokens` | body | `number` | no | Maximum number of tokens to generate. |
| `stream` | body | `boolean` | no | Whether to stream partial progress. |
| `stop` | body | `string` | no | Stop generation when a token or one of the provided tokens is detected. |
| `random_seed` | body | `number` | no | Seed to use for deterministic random sampling. |
| `prompt_mode` | body | `string` | no | Prompt behavior mode such as reasoning. |
| `response_format` | body | `object` | no | Structured output format settings. |
| `tools[]` | body | `array<object>` | no | Tool definitions available to the agent. |
| `tool_choice` | body | `string` | no | Tool selection behavior for the completion. |
| `parallel_tool_calls` | body | `boolean` | no | Allow the agent to call tools in parallel. |
| `metadata` | body | `object` | no | Optional metadata object for the request. |
| `prediction` | body | `object` | no | Expected completion content for response-time optimization. |
| `presence_penalty` | body | `number` | no | Penalty that encourages topic diversity. |
| `frequency_penalty` | body | `number` | no | Penalty that discourages repetition. |
| `n` | body | `number` | no | Number of completions to return. |
