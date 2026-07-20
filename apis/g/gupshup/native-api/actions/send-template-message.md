# Send Template Message with Gupshup

Sends a template WhatsApp message through Gupshup.

## Endpoint

- **Method:** `POST`
- **Path:** `/wa/api/v1/template/msg`
- **Base URL:** `https://api.gupshup.io`
- **Official documentation:** [Send Template Message](https://docs.gupshup.io/docs/template-messages)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `source` | body | `string` | yes | Registered WhatsApp Business API phone number. |
| `destination` | body | `string` | yes | User phone number to send the WhatsApp template message to. |
| `template` | body | `object` | yes | Template object with template ID and ordered parameter values. |
| `message` | body | `object` | no | Optional media or location object for media/location template messages. |
| `src.name` | body | `string` | no | Gupshup app name registered against the source phone number, when required by the selected template flow. |
