# Send SMS Link with SMSup

## Endpoint

- **Method:** `POST`
- **Path:** `/api/3.0/sms/send-link`
- **Base URL:** `https://api.gateway360.com`
- **Official documentation:** [Send SMS Link](https://app.smsup.es/api/3.0/docs/link/send)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array of messages to send. |
| `from` | body | `string` | yes | Originator address (sender). |
| `to` | body | `string` | yes | Destination mobile number in international format. |
| `text` | body | `string` | yes | Body of the text message including the {LINK} tag. |
| `link` | body | `string` | yes | URL to track when the recipient opens it. |
| `report_url` | body | `string` | no | URL where delivery and open events should be sent. |
| `fake` | body | `number` | no | Set to 1 to simulate submission without cost. |
