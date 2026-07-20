# Send SMS Campaign with ClickSend SMS

Creates and sends an SMS campaign in ClickSend SMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/sms-campaigns/send`
- **Base URL:** `https://rest.clicksend.com`
- **Official documentation:** [Send SMS Campaign](https://developers.clicksend.com/docs/messaging/sms-campaigns/send-sms-campaign/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `list_id` | body | `number` | yes |
| `name` | body | `string` | yes |
| `from` | body | `string` | yes |
| `body` | body | `string` | yes |
| `senders` | body | `list<object>` | yes |
| `senders[].recipient_country_code` | body | `string` | no |
| `senders[].sender_id` | body | `string` | no |
| `senders[].sender_type` | body | `string` | no |
| `senders[].sender_country_code` | body | `string` | no |
| `source` | body | `string` | no |
| `schedule` | body | `number` | no |
| `url_to_shorten` | body | `string` | no |
