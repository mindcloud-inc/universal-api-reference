# Send SMS to Contacts with SendMe

## Endpoint

- **Method:** `POST`
- **Path:** `/api/messages/sms/contacts`
- **Base URL:** `https://app.sendme123.com`
- **Official documentation:** [Send SMS to Contacts](https://docs.sendme123.com/en/api/messages/sms-contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[]` | body | `array<string>` | yes | List of phone numbers. |
| `country` | body | `string` | no | ISO 3166-1 alpha-2 country code. |
| `message` | body | `string` | yes | SMS message content. |
| `type` | body | `string` | no | Message type. |
