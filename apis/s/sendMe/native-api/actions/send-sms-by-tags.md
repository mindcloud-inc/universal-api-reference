# Send SMS by Tags with SendMe

## Endpoint

- **Method:** `POST`
- **Path:** `/api/messages/sms/tags`
- **Base URL:** `https://app.sendme123.com`
- **Official documentation:** [Send SMS by Tags](https://docs.sendme123.com/en/api/messages/sms-tags/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | ISO 3166-1 alpha-2 country code. |
| `message` | body | `string` | yes | SMS message content. |
| `tagIds[]` | body | `array<string>` | yes | List of tag IDs. |
| `type` | body | `string` | no | Message type. |
