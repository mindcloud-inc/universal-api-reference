# Send SMS Landing with SMSup

## Endpoint

- **Method:** `POST`
- **Path:** `/api/3.0/sms/send-landing`
- **Base URL:** `https://api.gateway360.com`
- **Official documentation:** [Send SMS Landing](https://app.smsup.es/api/3.0/docs/landing/send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array of messages to send. |
| `from` | body | `string` | yes | Originator address (sender). |
| `to` | body | `string` | yes | Destination mobile number in international format. |
| `text` | body | `string` | yes | Body of the text message including the {LANDING} tag. |
| `landing_id` | body | `number` | yes | ID of the landing template created in the account. |
| `report_url` | body | `string` | no | URL where delivery and landing events should be sent. |
| `fake` | body | `number` | no | Set to 1 to simulate submission without cost. |
