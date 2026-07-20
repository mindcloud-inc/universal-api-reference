# Post Message with Sunshine Conversations

Creates a new message in a Sunshine Conversations conversation.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:appId/conversations/:conversationId/messages`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [Post Message](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `author` | body | `string` | no | Message author object. |
| `content` | body | `string` | no | Message content object. |
| `conversationId` | path | `string` | no | Conversation id. |
