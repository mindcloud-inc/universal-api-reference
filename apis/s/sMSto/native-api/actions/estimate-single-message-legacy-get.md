# Estimate Single Message Legacy GET with SMS.to

Retrieves a cost estimate for a single SMS message using SMS.to's legacy endpoint.

## Endpoint

- **Method:** `GET`
- **Path:** `/sms/estimate`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Estimate Single Message Legacy GET](https://developers.sms.to/#1e976374-8553-45e3-b84b-388494d7cb7b)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | query | `string` | yes | Your message. |
| `to` | query | `string` | yes | Phone number. |
| `sender_id` | query | `string` | no | The displayed value of who sent the message. |
