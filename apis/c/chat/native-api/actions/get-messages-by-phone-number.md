# Get Messages by Phone Number with 2Chat

Retrieves WhatsApp messages in 2Chat by phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/whatsapp/messages/:from_number/:remote_number`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Get Messages by Phone Number](https://developers.2chat.co/docs/API/WhatsApp/Web/messages/get-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_number` | path | `string` | yes | The WhatsApp number connected to 2Chat whose messages you want to fetch. |
| `remote_number` | path | `string` | no | Optional remote WhatsApp number to scope messages to one conversation. |
| `page_number` | query | `number` | no | Zero-based page number for older message pages. |
