# Send Single Message with SMS.to

Sends a single SMS message through SMS.to.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/send`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Send Single Message](https://developers.sms.to/#3a12f9ae-8afa-4d15-a3c5-4895c3a14778)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `to` | body | `string` | yes | Phone number. |
| `bypass_optout` | body | `boolean` | no | True will bypass opt-outs. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
| `callback_url` | body | `string` | no | A callback URL for message status updates. |
