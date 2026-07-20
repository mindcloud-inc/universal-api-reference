# Get a Message with 2Chat

Retrieves a WhatsApp message from 2Chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/whatsapp/message/:session_key/:message_uuid`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Get a Message](https://developers.2chat.co/docs/API/WhatsApp/Web/messages/get-single-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_key` | path | `string` | yes | The WhatsApp session key that owns the message. |
| `message_uuid` | path | `string` | yes | The UUID of the message to retrieve. |
