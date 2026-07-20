# Add to Agent Blacklist with Chatvolt AI

Adds an agent blacklist entry in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/agent-blacklist`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Add to Agent Blacklist](https://docs.chatvolt.ai/api-reference/endpoint/agents/post-agent-blacklist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | body | `string` | yes | The ID of the agent. |
| `userIdentify` | body | `string` | yes | UserIdentify for application/json requests. |
