# Get contact with Bulldog-WP

Retrieves a contact from Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/chat/{deviceId}/contacts/{contactWid}`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [Get contact](https://console.bulldog-wp.co.il/docs/specification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactWid` | path | `string` | yes | WhatsApp contact ID or phone number. |
| `deviceId` | path | `string` | yes | WhatsApp number device ID from Bulldog WP. |
