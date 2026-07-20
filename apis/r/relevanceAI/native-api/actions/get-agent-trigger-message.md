# Get Agent Trigger Message with Relevance AI

## Endpoint

- **Method:** `GET`
- **Path:** `/agents/:agentId/tasks/:conversationId/trigger_message`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [Get Agent Trigger Message](https://sdk.relevanceai.com/concepts/10_1/agents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The Relevance AI agent id. |
| `conversationId` | path | `string` | yes | The task or conversation id. |
