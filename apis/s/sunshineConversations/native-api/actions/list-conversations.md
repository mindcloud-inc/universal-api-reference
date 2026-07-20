# List Conversations with Sunshine Conversations

Retrieves app conversations from Sunshine Conversations.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/:appId/conversations`
- **Base URL:** `https://api.smooch.io/v2`
- **Official documentation:** [List Conversations](https://developer.zendesk.com/api-reference/conversations/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | no | Sunshine Conversations app id. |
| `filter[userId]` | query | `string` | no | Filter conversations by participant user id. |
