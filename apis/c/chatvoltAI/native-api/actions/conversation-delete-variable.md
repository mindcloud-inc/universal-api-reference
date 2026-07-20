# Delete Custom Variable with Chatvolt AI

Deletes a custom variable from Chatvolt AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/variables/{conversationId}/{varName}`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Delete Custom Variable](https://docs.chatvolt.ai/api-reference/endpoint/conversation/delete-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | Conversation ID. |
| `varName` | path | `string` | yes | Name of the variable to be deleted. |
