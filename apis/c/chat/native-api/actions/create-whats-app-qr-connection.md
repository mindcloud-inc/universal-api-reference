# Create WhatsApp QR Connection with 2Chat

Creates a WhatsApp QR connection in 2Chat.

## Endpoint

- **Method:** `POST`
- **Path:** `/whatsapp/channel/create`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Create WhatsApp QR Connection](https://developers.2chat.co/docs/API/WhatsApp/Web/channel/create-whatsapp-qr-connection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone_number` | body | `string` | yes | The WhatsApp phone number to connect to 2Chat. |
| `friendly_name` | body | `string` | yes | A friendly label for the connected number. |
