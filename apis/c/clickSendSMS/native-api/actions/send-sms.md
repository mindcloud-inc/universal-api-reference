# Send SMS with ClickSend SMS

Creates a new SMS message in ClickSend SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/sms/send`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Send SMS](https://developers.clicksend.com/docs/messaging/sms/other/send-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array payload for /v3/sms/send. Each object includes required to and body fields plus optional source, from, schedule, custom_string, and country. |
| `messages[].to` | body | `string` | yes | Destination phone number in international format. |
| `messages[].body` | body | `string` | yes | SMS content text. |
| `messages[].from` | body | `string` | no | Sender ID or originating number where supported. |
| `messages[].source` | body | `string` | no | Source identifier, for example 'sdk'. |
| `messages[].schedule` | body | `string` | no | Scheduled send time where supported by provider format. |
| `messages[].custom_string` | body | `string` | no | Custom tracking metadata string. |
| `messages[].country` | body | `string` | no | Country code override for destination handling. |
