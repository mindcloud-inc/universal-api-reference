# List User Messages with Chatforma

Retrieves user message records from Chatforma.

## Endpoint

- **Method:** `GET`
- **Path:** `/bots/:botId/dialogs/:userId/messages`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [List User Messages](https://docs.chatforma.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `botId` | path | `number` | yes |
| `userId` | path | `number` | yes |
