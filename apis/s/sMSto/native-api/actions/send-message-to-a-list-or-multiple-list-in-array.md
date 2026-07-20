# Send Message to a List or Multiple List in Array with SMS.to

Sends an SMS message to one or more lists.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/send`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Send Message to a List or Multiple List in Array](https://developers.sms.to/#5ccea815-9f65-428f-8c17-97514825b4b4)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `list_id` | body | `string` | yes | List identifier. |
| `bypass_optout` | body | `boolean` | no | True will bypass opt-outs. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
| `callback_url` | body | `string` | no | A callback URL for message status updates. |
