# Send SMS with Aloware

Sends an SMS or MMS message from Aloware.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhook/sms-gateway/send`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [Send SMS](https://support.aloware.com/en/articles/9020040-api-documentation-aloware-sms-api-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Sender phone number. Provide this or Line ID. |
| `line_id` | body | `string` | no | Aloware line ID to send from. Provide this or From Number. |
| `to` | body | `string` | yes | Recipient phone number. |
| `message` | body | `string` | yes | SMS or MMS message content. |
| `image_url` | body | `string` | no | Optional image URL to send as MMS. |
| `force_random` | body | `string` | no | Set to 1 to ignore number stickiness and distribute randomly. |
