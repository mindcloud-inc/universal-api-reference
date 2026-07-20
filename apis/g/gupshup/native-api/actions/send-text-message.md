# Send Text Message with Gupshup

Sends a text WhatsApp message through Gupshup.

## Endpoint

- **Method:** `POST`
- **Path:** `/wa/api/v1/msg`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Send Text Message](https://docs.gupshup.io/reference/msg)

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
| `message` | body | `string` | no | Text message object, for example a Gupshup object with type `text` and text content. |
| `source` | body | `string` | no | Registered WhatsApp Business API phone number. |
| `src.name` | body | `string` | no | Gupshup app name registered against the source phone number. |
