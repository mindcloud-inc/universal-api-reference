# Create Contact with Pingdom

## Endpoint

- **Method:** `POST`
- **Path:** `/alerting/contacts`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [Create Contact](https://docs.pingdom.com/api/#tag/Contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Contact name. |
| `paused` | body | `boolean` | no | Pause or unpause notifications for the contact. |
| `notification_targets.email[]` | body | `array<object>` | no | Email notification targets as an array of objects with severity and address. |
| `notification_targets.sms[]` | body | `array<object>` | no | SMS notification targets as an array of objects with severity, country_code, number, and provider. |
