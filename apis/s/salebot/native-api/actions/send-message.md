# Send Message with Salebot

## Endpoint

- **Method:** `POST`
- **Path:** `/message`
- **Base URL:** `https://chatter.salebot.pro/api/{apiKey}`
- **Official documentation:** [Send Message](https://docs.salebot.pro/rabota-s-api/api-konstruktora)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | body | `number` | yes | Existing Salebot client ID. |
| `message_id` | body | `number` | no | Bot block ID to send instead of raw text. |
| `message` | body | `string` | no | Message text to send. |
| `attachment_url` | body | `string` | no | Public file URL to attach. |
| `attachment_type` | body | `string` | no | Attachment rendering type: image, video, link, file, or audio. |
