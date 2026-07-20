# Get One Custom Variable with Chatvolt AI

Retrieves a custom variable from Chatvolt AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/variables/{conversationId}/{varName}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Get One Custom Variable](https://docs.chatvolt.ai/api-reference/endpoint/conversation/get-one-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | Conversation ID. |
| `varName` | path | `string` | yes | Variable name. |
