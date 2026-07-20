# Delete Conversation with Sunshine Conversations

Deletes a conversation, its messages, and attachments from Sunshine Conversations.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/apps/:appId/conversations/:conversationId`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [Delete Conversation](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `conversationId` | path | `string` | no | Conversation id. |
