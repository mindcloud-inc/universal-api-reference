# Continue Agent Conversation with Chaindesk

Sends a follow-up query in a Chaindesk conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/agents/:agentId/query`
- **Base URL:** `https://app.chaindesk.ai/api`
- **Official documentation:** [Continue Agent Conversation](https://docs.chaindesk.ai/api-reference/endpoint/agents/query)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentId` | path | `string` | yes |
| `conversationId` | body | `string` | yes |
| `query` | body | `string` | yes |
