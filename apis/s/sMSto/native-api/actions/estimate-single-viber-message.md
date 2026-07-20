# Estimate Single Viber Message with SMS.to

Retrieves a cost estimate for a single Viber message.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/estimate`
- **Base URL:** `https://api.sms.to`
- **Official documentation:** [Estimate Single Viber Message](https://developers.sms.to/#13d6ed83-cc16-4d78-a26f-50ce942eb58d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `message` | body | `string` | yes | Your message. |
| `to` | body | `string` | yes | Phone number. |
