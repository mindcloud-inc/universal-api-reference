# List Active Chats with GoSquared

Retrieves active chats for a GoSquared site.

## Endpoint

- **Method:** `GET`
- **Path:** `chat/v1/chats`
- **Base URL:** `https://api.gosquared.com`
- **Official documentation:** [List Active Chats](https://www.gosquared.com/docs/chat/chats/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Optional start date-time for the chat query. |
| `to` | query | `string` | no | Optional end date-time for the chat query. |
