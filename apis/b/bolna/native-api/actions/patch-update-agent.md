# Patch Update Agent with Bolna

Updates selected fields on an existing Bolna voice AI agent.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/agent/:agentId`
- **Base URL:** `https://api.bolna.ai`
- **Official documentation:** [Patch Update Agent](https://www.bolna.ai/docs/api-reference/agent/v2/patch_update)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | path | `string` | yes | The ID of the agent. |
| `agent_config` | body | `object` | no | Partial agent configuration payload. |
| `agent_prompts` | body | `object` | no | Partial prompt payload keyed by task id. |
