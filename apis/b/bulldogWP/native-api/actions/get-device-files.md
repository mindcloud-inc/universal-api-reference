# Search inbound files with Bulldog-WP

Finds inbound files in Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/{deviceId}/files`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Search inbound files](https://console.bulldog-wp.co.il/docs/specification)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | WhatsApp number device ID from Bulldog WP. |
