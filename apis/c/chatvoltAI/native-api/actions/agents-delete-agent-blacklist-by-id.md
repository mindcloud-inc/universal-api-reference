# Delete Agent Blacklist Entry with Chatvolt AI

Deletes an agent blacklist entry from Chatvolt AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/agent-blacklist/{agentId}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Delete Agent Blacklist Entry](https://docs.chatvolt.ai/api-reference/endpoint/agents/delete-agent-blacklist-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The ID of the agent associated with the blacklist (required for path, but not used in delete logic). |
| `id` | query | `string` | yes | The ID of the blacklist entry to delete. |
