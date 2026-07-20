# Send Image with WhatsScale

Sends an image message through WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sendImage`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Send Image](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caption` | body | `string` | no | Optional image caption. |
| `chatId` | body | `string` | yes | Recipient chat ID. |
| `file` | body | `string` | yes | Public URL to the image. |
| `session` | body | `string` | yes | Session name from /api/sessions. |
