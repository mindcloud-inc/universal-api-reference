# Estimate Campaign Message with SMS.to

Retrieves a cost estimate for a bulk SMS campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/estimate`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Estimate Campaign Message](https://developers.sms.to/#ee7a8f3c-d4bb-4cd0-a6ce-3b62c3f9530f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
| `to[]` | body | `array<string>` | yes | Array of phone numbers. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
