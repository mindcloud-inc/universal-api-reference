# List Messages with Sunshine Conversations

Retrieves messages from a Sunshine Conversations conversation.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:appId/conversations/:conversationId/messages`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [List Messages](https://developer.zendesk.com/api-reference/conversations/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `conversationId` | path | `string` | no | Conversation id. |
