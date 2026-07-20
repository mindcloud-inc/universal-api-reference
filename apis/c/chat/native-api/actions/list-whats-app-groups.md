# List WhatsApp Groups with 2Chat

Retrieves WhatsApp groups from 2Chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/whatsapp/groups/:from_number`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [List WhatsApp Groups](https://developers.2chat.co/docs/API/WhatsApp/Web/groups/list-whatsapp-groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from_number` | path | `string` | yes | The WhatsApp number connected to 2Chat whose groups you want to list. |
