# Send SMS to All with SendMe

## Endpoint

- **Method:** `POST`
- **Path:** `/api/messages/sms/all`
- **Base URL:** `https://app.sendme123.com`
- **Official documentation:** [Send SMS to All](https://docs.sendme123.com/en/api/messages/sms-all/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | body | `string` | no | ISO 3166-1 alpha-2 country code. |
| `message` | body | `string` | yes | SMS message content. |
| `type` | body | `string` | no | Message type. |
