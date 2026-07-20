# Update Contact with Pingdom

## Endpoint

- **Method:** `PUT`
- **Path:** `/alerting/contacts/:contactid`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [Update Contact](https://docs.pingdom.com/api/#tag/Contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactid` | path | `number` | yes | Identifier of the contact. |
| `name` | body | `string` | yes | Contact name. |
| `paused` | body | `boolean` | yes | Pause or unpause notifications for the contact. |
| `notification_targets.email[]` | body | `array<object>` | no | Email notification targets as an array of objects with severity and address. |
| `notification_targets.sms[]` | body | `array<object>` | no | SMS notification targets as an array of objects with severity, country_code, number, and provider. |
