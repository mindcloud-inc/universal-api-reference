# Set Priority with Chatvolt AI

Sets a conversation priority in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/{conversationId}/set-priority`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Set Priority](https://docs.chatvolt.ai/api-reference/endpoint/conversation/set-priority)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ID of the conversation for which the priority will be set. |
| `priority` | body | `string` | yes | New priority for the conversation. |
