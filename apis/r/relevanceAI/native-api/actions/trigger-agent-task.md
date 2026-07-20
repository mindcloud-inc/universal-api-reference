# Trigger Agent Task with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/trigger`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [Trigger Agent Task](https://sdk.relevanceai.com/concepts/10_1/agents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | yes | The Relevance AI agent id to trigger. |
| `message.role` | body | `string` | no | Role for the nested provider message object. |
| `message.content` | body | `string` | yes | The user message to send to the agent. |
