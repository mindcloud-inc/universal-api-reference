# Send Viber Message with D7 Messaging

Sends a Viber message through D7 Messaging.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/v1/send`
- **Base URL:** `https://api.d7networks.com`
- **Official documentation:** [Send Viber Message](https://d7networks.com/docs/viber/send-viber-message/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message_globals.originator` | body | `string` | yes | Sender name shown to the recipient in Viber. |
| `messages[].recipients[]` | body | `array<string>` | yes | One or more Viber recipient mobile numbers in E.164 format including country code. |
| `messages[].content` | body | `string` | yes | Viber message body. |
| `messages[].label` | body | `string` | no | Viber message category such as PROMOTION. |
| `message_globals.call_back_url` | body | `string` | no | Webhook URL to receive delivery callbacks for this Viber message. |
