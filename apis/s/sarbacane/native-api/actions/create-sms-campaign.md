# Create SMS Campaign with Sarbacane

Creates a new SMS campaign in Sarbacane.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/sms`
- **Base URL:** `https://api.sarbacane.com/v1`
- **Official documentation:** [Create SMS Campaign](https://developers.sarbacane.com/campaigns/#create-a-sms-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | SMS content. |
| `kind` | body | `string` | no | SMS campaign kind: SMS_MARKETING or SMS_NOTIFICATION. |
| `name` | body | `string` | no | Campaign name. |
| `smsFrom` | body | `string` | no | Optional SMS sender name. |
