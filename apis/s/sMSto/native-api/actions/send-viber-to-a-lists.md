# Send Viber to a List/s with SMS.to

Sends a Viber message to one or more lists.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/send`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Send Viber to a List/s](https://developers.sms.to/#1c01abb9-f7dc-4dfc-9481-6bb5e31f4c97)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `list_id` | body | `string` | yes | List identifier. |
| `bypass_optout` | body | `boolean` | no | True will bypass opt-outs. |
| `callback_url` | body | `string` | no | A callback URL for message status updates. |
