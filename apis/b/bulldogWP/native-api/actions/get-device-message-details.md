# Get message details with Bulldog-WP

Retrieves message details from Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/{deviceId}/messages/{messageWid}`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Get message details](https://console.bulldog-wp.co.il/docs/specification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | WhatsApp number device ID from Bulldog WP. |
| `messageWid` | path | `string` | yes | WhatsApp message ID. |
