# Delete Message with Sunshine Conversations

Deletes a message from a Sunshine Conversations conversation.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/apps/:appId/conversations/:conversationId/messages/:messageId`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [Delete Message](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `conversationId` | path | `string` | no | Conversation id. |
| `messageId` | path | `string` | no | Message id. |
