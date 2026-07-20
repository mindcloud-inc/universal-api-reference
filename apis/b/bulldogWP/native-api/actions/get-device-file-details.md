# Get inbound file details with Bulldog-WP

Retrieves inbound file details from Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/{deviceId}/files/{fileId}`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Get inbound file details](https://console.bulldog-wp.co.il/docs/specification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceId` | path | `string` | yes | WhatsApp number device ID from Bulldog WP. |
| `fileId` | path | `string` | yes | Inbound file resource ID. |
