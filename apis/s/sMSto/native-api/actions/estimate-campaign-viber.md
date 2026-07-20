# Estimate Campaign Viber with SMS.to

Retrieves a cost estimate for a Viber campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/estimate`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Estimate Campaign Viber](https://developers.sms.to/#cf0b6175-236b-4a47-bc8b-1bab933373df)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `to[]` | body | `array<string>` | yes | Array of phone numbers. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
