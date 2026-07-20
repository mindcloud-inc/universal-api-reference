# Send Personalized Messages with SMS.to

Sends personalized SMS messages to multiple recipients.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/send`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Send Personalized Messages](https://developers.sms.to/#7abcccad-8066-403e-9bfc-515e3bd6f8f2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array of message objects with recipient phone numbers. |
| `messages[].message` | body | `string` | yes | Your message for the specified phone number. |
| `messages[].to` | body | `string` | yes | The recipient phone number. |
| `messages[].bypass_optout` | body | `boolean` | no | True will bypass opt-outs. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
| `callback_url` | body | `string` | no | A callback URL for message status updates. |
