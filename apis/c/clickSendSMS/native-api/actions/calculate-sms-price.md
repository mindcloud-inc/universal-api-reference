# Calculate SMS Price with ClickSend SMS

Calculates SMS pricing in ClickSend SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/sms/price`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Calculate SMS Price](https://developers.clicksend.com/docs/messaging/sms/other/calculate-sms-price)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `messages[]` | body | `array<object>` | yes | Array payload for /v3/sms/price. Each object includes required to and body plus optional source, from, schedule, custom_string, and country. |
| `messages[].to` | body | `string` | yes | Destination phone number in international format. |
| `messages[].body` | body | `string` | yes | SMS content text used for pricing. |
| `messages[].from` | body | `string` | no | Sender ID or originating number where supported. |
| `messages[].source` | body | `string` | no | Source identifier, for example 'sdk'. |
| `messages[].schedule` | body | `string` | no | Scheduled send time where supported by provider format. |
| `messages[].custom_string` | body | `string` | no | Custom tracking metadata string. |
| `messages[].country` | body | `string` | no | Country code override for destination handling. |
