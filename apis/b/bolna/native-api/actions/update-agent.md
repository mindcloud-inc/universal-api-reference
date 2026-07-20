# Update Agent with Bolna

Updates an existing voice AI agent in Bolna.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/agent/:agentId`
- **Base URL:** `https://api.bolna.ai`
- **Official documentation:** [Update Agent](https://www.bolna.ai/docs/api-reference/agent/v2/update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The ID of the agent. |
| `agent_config` | body | `object` | yes | Full replacement configuration payload for the agent. |
| `agent_prompts` | body | `object` | yes | Full replacement prompt payload keyed by task id. |
