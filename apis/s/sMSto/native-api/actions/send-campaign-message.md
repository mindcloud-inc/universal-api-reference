# Send Campaign Message with SMS.to

Sends an SMS campaign to multiple recipients in SMS.to.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/send`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Send Campaign Message](https://developers.sms.to/#436bf9d3-0c63-48ac-9a54-91f7d239a86f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `to[]` | body | `array<string>` | yes | Array of phone numbers. |
| `bypass_optout` | body | `boolean` | no | True will bypass opt-outs. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
| `callback_url` | body | `string` | no | A callback URL for message status updates. |
