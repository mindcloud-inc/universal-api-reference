# View Task Steps with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/:agentId/tasks/:conversationId/view`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [View Task Steps](https://sdk.relevanceai.com/concepts/10_1/agents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agentId` | path | `string` | yes | The Relevance AI agent id. |
| `conversationId` | path | `string` | yes | The task or conversation id to inspect. |
