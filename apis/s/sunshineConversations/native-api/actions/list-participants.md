# List Participants with Sunshine Conversations

Retrieves conversation participants from Sunshine Conversations.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:appId/conversations/:conversationId/participants`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [List Participants](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `conversationId` | path | `string` | no | Conversation id. |
