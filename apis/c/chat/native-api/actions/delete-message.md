# Delete Message with 2Chat

Deletes a WhatsApp message from 2Chat.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/whatsapp/message/:session_key/:message_uuid`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Delete Message](https://developers.2chat.co/docs/API/WhatsApp/Web/messages/delete-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_key` | path | `string` | yes | The WhatsApp session key that owns the message. |
| `message_uuid` | path | `string` | yes | The UUID of the message to delete. |
