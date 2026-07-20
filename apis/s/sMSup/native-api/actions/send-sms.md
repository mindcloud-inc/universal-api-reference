# Send SMS with SMSup

## Endpoint

- **Method:** `POST`
- **Path:** `/api/3.0/sms/send`
- **Base URL:** `https://api.gateway360.com`
- **Official documentation:** [Send SMS](https://app.smsup.es/api/3.0/docs/sms/send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array of messages to send. |
| `from` | body | `string` | yes | Originator address (sender). |
| `to` | body | `string` | yes | Destination mobile number in international format. |
| `text` | body | `string` | yes | Body of the text message. |
| `report_url` | body | `string` | no | URL where delivery reports should be sent. |
| `fake` | body | `number` | no | Set to 1 to simulate submission without cost. |
