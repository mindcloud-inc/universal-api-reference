# Send Viber Message with D7 Networks

Sends a Viber message with D7 Networks.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/v1/send`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Send Viber Message](https://d7networks.com/docs/viber/send-viber-message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[].originator` | body | `string` | yes | Approved Viber sender/originator. |
| `messages[].recipients[]` | body | `array<string>` | yes | Recipient phone numbers with country codes. |
| `messages[].content` | body | `string` | yes | Viber message text. |
| `message_globals.report_url` | body | `string` | no | Optional delivery report webhook URL. |
| `message_globals.tag` | body | `string` | no | Optional client reference tag. |
