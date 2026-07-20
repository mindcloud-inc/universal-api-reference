# List Chat Messages with Microsoft Teams

Retrieves chat messages from Microsoft Teams.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/chats/:chatId/messages`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Chat Messages](https://learn.microsoft.com/en-us/graph/api/chat-list-messages?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | Microsoft Graph chat ID. |
