# Update Conversation with Sunshine Conversations

Updates an existing conversation in Sunshine Conversations.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/apps/:appId/conversations/:conversationId`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [Update Conversation](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `conversationId` | path | `string` | no | Conversation id. |
| `displayName` | body | `string` | no | Conversation display name. |
