# Send Message with Gupshup

Sends a WhatsApp message through Gupshup.

## Endpoint

- **Method:** `POST`
- **Path:** `/wa/api/v1/msg`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Send Message](https://docs.gupshup.io/reference/msg)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `string` | yes | Registered WhatsApp Business API phone number. |
| `destination` | body | `string` | yes | User phone number to send the WhatsApp message to. |
| `message` | body | `object` | yes | Gupshup message object for the selected message type. |
| `src.name` | body | `string` | yes | Gupshup app name registered against the source phone number. |
