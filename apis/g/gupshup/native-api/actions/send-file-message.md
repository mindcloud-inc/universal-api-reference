# Send File Message with Gupshup

Sends a file WhatsApp message through Gupshup.

## Endpoint

- **Method:** `POST`
- **Path:** `/wa/api/v1/msg`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Send File Message](https://docs.gupshup.io/reference/msg)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `string` | no | Messaging channel. Gupshup WhatsApp send APIs use `whatsapp`. |
| `destination` | body | `string` | no | User phone number to send the WhatsApp message to. |
| `message` | body | `string` | no | File/document message object, including URL and filename as documented by Gupshup. |
| `source` | body | `string` | no | Registered WhatsApp Business API phone number. |
| `src.name` | body | `string` | no | Gupshup app name registered against the source phone number. |
