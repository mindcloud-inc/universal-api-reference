# Approve Task with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/trigger`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [Approve Task](https://sdk.relevanceai.com/concepts/10_1/agents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agent_id` | body | `string` | yes |
| `conversation_id` | body | `string` | yes |
| `message.action` | body | `string` | yes |
| `message.action_request_id` | body | `string` | yes |
