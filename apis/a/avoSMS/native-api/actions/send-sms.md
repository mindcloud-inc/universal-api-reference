# Send SMS with AvoSMS

Sends an SMS with AvoSMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sms/send`
- **Base URL:** `https://api.avosms.com`
- **Official documentation:** [Send SMS](https://www.avosms.com/en/api/documentation/sms/send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipients` | body | `string` | yes | Recipient phone numbers |
| `message` | body | `string` | yes | SMS content up to 600 characters |
| `sender` | body | `string` | no | Sender name between 3 and 11 characters |
| `deliveryDate` | body | `string` | no | Desired sending date in DD/MM/YYYY format |
| `deliveryHour` | body | `string` | no | Desired sending time |
| `type` | body | `string` | no | SMS type: N for notification or M for marketing |
| `clickFollow` | body | `string` | no | 0 to disable click tracking, 1 to enable |
