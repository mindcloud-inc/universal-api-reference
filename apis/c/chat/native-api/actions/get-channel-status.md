# Get Channel Status with 2Chat

Retrieves a WhatsApp channel status from 2Chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/whatsapp/channel/:channel_uuid/status`
- **Base URL:** `https://api.p.2chat.io/open`
- **Official documentation:** [Get Channel Status](https://developers.2chat.co/docs/API/WhatsApp/Web/channel/get-channel-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_uuid` | path | `string` | yes | The UUID of the WhatsApp channel connected to 2Chat. |
