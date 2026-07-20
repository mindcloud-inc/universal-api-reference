# Create Conversation with Sunshine Conversations

Creates a new conversation in Sunshine Conversations.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:appId/conversations`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [Create Conversation](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `displayName` | body | `string` | no | Conversation display name. |
| `participants` | body | `string` | no | Conversation participants array. |
| `type` | body | `string` | no | Conversation type. |
