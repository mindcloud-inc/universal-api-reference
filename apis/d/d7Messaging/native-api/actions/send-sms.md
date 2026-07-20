# Send SMS with D7 Messaging

Sends an SMS message through D7 Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/v1/send`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Send SMS](https://d7networks.com/docs/sms/send-sms/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_globals.originator` | body | `string` | yes | Brand name or sender number displayed to the recipient. |
| `messages[].recipients[]` | body | `array<string>` | yes | One or more recipient mobile numbers in E.164 format including country code. |
| `messages[].content` | body | `string` | yes | SMS message body. |
| `message_globals.report_url` | body | `string` | no | Webhook URL to receive delivery reports for this message. |
| `messages[].data_coding` | body | `string` | no | Encoding mode for the SMS content: text, unicode, or auto. |
