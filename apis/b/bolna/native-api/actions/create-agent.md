# Create Agent with Bolna

Creates a new voice AI agent in Bolna.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/agent`
- **Base URL:** `https://api.bolna.ai`
- **Official documentation:** [Create Agent](https://www.bolna.ai/docs/api-reference/agent/v2/create)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_config` | body | `object` | yes | Configuration payload for the agent. |
| `agent_prompts` | body | `object` | yes | Prompt payload keyed by task id. |
