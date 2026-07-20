# Send Flash Message with SMS.to

Sends a single flash SMS message through SMS.to.

## Endpoint

- **Method:** `POST`
- **Path:** `/fsms/send`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Send Flash Message](https://developers.sms.to/#f166ed5d-c461-471c-be14-8d79d61049b8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `to` | body | `string` | yes | Phone number. |
| `bypass_optout` | body | `boolean` | no | True will bypass opt-outs. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
| `callback_url` | body | `string` | no | A callback URL for message status updates. |
