# List Bot Users with Chatforma

Retrieves bot user records from Chatforma.

## Endpoint

- **Method:** `GET`
- **Path:** `/bots/:botId/users`
- **Base URL:** `https://api.pro.chatforma.com/public/v1`
- **Official documentation:** [List Bot Users](https://docs.chatforma.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `number` | yes | — |
| `deleted` | query | `number` | no | Set to show only deleted users. |
