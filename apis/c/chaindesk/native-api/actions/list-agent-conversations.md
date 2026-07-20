# List Agent Conversations with Chaindesk

Retrieves conversations for an agent in Chaindesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://app.chaindesk.ai/api`
- **Official documentation:** [List Agent Conversations](https://docs.chaindesk.ai/api-reference/endpoint/conversations/get)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `agentId` | query | `string` | yes |
| `take` | query | `number` | no |
