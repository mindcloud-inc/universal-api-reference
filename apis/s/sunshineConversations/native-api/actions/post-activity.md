# Post Activity with Sunshine Conversations

Posts conversation activity events to Sunshine Conversations.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/:appId/conversations/:conversationId/activity`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [Post Activity](https://developer.zendesk.com/api-reference/conversations/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activity` | body | `string` | no | Activity object. |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `author` | body | `string` | no | Activity author object. |
| `conversationId` | path | `string` | no | Conversation id. |
