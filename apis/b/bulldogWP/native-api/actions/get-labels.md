# List labels with Bulldog-WP

Retrieves labels from Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/devices/{deviceId}/labels`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [List labels](https://console.bulldog-wp.co.il/docs/specification)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | WhatsApp number device ID from Bulldog WP. |
