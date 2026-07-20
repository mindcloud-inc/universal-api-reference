# Search chats with Bulldog-WP

Finds chats in Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/{deviceId}/chats`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Search chats](https://console.bulldog-wp.co.il/docs/specification)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | WhatsApp number device ID from Bulldog WP. |
