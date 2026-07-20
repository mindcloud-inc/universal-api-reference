# Estimate List Message with SMS.to

Retrieves a cost estimate for an SMS list campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/estimate`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Estimate List Message](https://developers.sms.to/#34aedb6e-3d81-409e-a485-75c41f32fa04)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `list_id` | body | `string` | yes | List identifier. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
