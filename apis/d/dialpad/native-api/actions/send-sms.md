# Send SMS with Dialpad

Sends an SMS message from Dialpad.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [Send SMS](https://developers.dialpad.com/reference/smssend)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | no | The contents of the message that should be sent. |
| `to_numbers[]` | body | `array<string>` | no | Up to 10 E164-formatted phone numbers who should receive the SMS. |
| `user_id` | body | `number` | no | The ID of the user who should be the sender of the SMS. |
| `from_number` | body | `string` | no | The sender number. This overrides user_id and sender_group_id. |
| `sender_group_id` | body | `number` | no | The ID of an office, department, or call center that the user should send the message on behalf of. |
| `sender_group_type` | body | `string` | no | The sender group's type. |
| `channel_hashtag` | body | `string` | no | The hashtag of the channel which should receive the SMS. |
| `infer_country_code` | body | `boolean` | no | If true, to_numbers will be assumed to be from the specified user's country. |
| `media` | body | `string` | no | Base64-encoded media attachment. |
