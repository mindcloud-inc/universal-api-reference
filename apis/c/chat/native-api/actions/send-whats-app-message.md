# Send WhatsApp Message with 2Chat

Creates a WhatsApp message in 2Chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/send-message`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Send WhatsApp Message](https://developers.2chat.co/docs/API/WhatsApp/Web/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_number` | body | `string` | yes | The WhatsApp number connected to 2Chat that sends the message. |
| `to_number` | body | `string` | no | The WhatsApp phone number that receives the message. |
| `to_group_uuid` | body | `string` | no | The UUID of the WhatsApp group that receives the message. |
| `text` | body | `string` | no | The text content of the message. |
| `url` | body | `string` | no | A publicly accessible media file URL to attach. |
| `pin.latitude` | body | `string` | no | Latitude for an optional location pin. |
| `pin.longitude` | body | `string` | no | Longitude for an optional location pin. |
| `pin.name` | body | `string` | no | Name for an optional location pin. |
| `pin.address` | body | `string` | no | Address for an optional location pin. |
| `pin.url` | body | `string` | no | URL for an optional location pin. |
