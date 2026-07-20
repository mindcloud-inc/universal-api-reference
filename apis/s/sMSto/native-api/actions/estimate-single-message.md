# Estimate Single Message with SMS.to

Retrieves a cost estimate for a single SMS message.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/estimate`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Estimate Single Message](https://developers.sms.to/#dee1f2ba-a154-43da-aa88-80cd4841a6da)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `to` | body | `string` | yes | Phone number. |
| `sender_id` | body | `string` | no | The displayed value of who sent the message. |
