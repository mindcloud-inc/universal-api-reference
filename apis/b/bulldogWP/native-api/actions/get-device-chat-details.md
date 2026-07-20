# Get chat by WID with Bulldog-WP

Retrieves a chat from Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/{deviceId}/chats/{chatWid}`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Get chat by WID](https://console.bulldog-wp.co.il/docs/specification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatWid` | path | `string` | yes | WhatsApp chat ID. |
| `deviceId` | path | `string` | yes | WhatsApp number device ID from Bulldog WP. |
