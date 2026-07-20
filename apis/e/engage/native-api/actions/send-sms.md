# Send SMS with Engage

Sends a transactional SMS through Engage.

## Endpoint

- **Method:** `POST`
- **Path:** `/send/sms`
- **Base URL:** `https://api.engage.so/v1`
- **Official documentation:** [Send SMS](https://docs.engage.so/en-us/a/650f5a1ba36d1df032bd73aa-transactional-messaging#send-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `string` | no | Optional SMS channel, such as generic or dnd for supported providers. |
| `from` | body | `string` | yes | Sender ID registered with your SMS provider. |
| `track_clicks` | body | `boolean` | no | Set to true to enable click tracking. |
| `source` | body | `string` | yes | SMS integration to send with, such as twilio or termii. |
| `to` | body | `string` | yes | Recipient phone number with country code. |
| `body` | body | `string` | yes | Message body. |
