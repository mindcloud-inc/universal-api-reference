# Send SMS with D7 Networks

Sends an SMS message with D7 Networks.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/v1/send`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Send SMS](https://d7networks.com/docs/sms/send-sms/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[].recipients[]` | body | `array<string>` | yes | Mobile numbers with country codes to receive the SMS. |
| `messages[].content` | body | `string` | yes | Text message content. |
| `message_globals.originator` | body | `string` | yes | Sender ID or brand name shown to the recipient. |
| `message_globals.report_url` | body | `string` | no | Optional delivery report webhook URL. |
| `message_globals.tag` | body | `string` | no | Optional client reference tag for the message. |
