# Send Campaign Viber with SMS.to

Sends a Viber campaign to multiple recipients in SMS.to.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/send`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Send Campaign Viber](https://developers.sms.to/#84e486e1-a3d6-4eab-be1b-111d3ada129f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `to[]` | body | `array<string>` | yes | Array of phone numbers. |
| `bypass_optout` | body | `boolean` | no | True will bypass opt-outs. |
| `callback_url` | body | `string` | no | A callback URL for message status updates. |
