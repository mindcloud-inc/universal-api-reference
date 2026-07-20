# Update Status with Chatvolt AI

Updates a conversation status in Chatvolt AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/{conversationId}/set-status`
- **Base URL:** `https://api.chatvolt.ai`
- **Official documentation:** [Update Status](https://docs.chatvolt.ai/api-reference/endpoint/conversation/update-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversationId` | path | `string` | yes | ID of the conversation for which the status will be set. |
| `status` | body | `string` | yes | New status for the conversation. |
