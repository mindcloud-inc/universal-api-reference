# Send Video with WhatsScale

Creates a video send job in WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sendVideo`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Send Video](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caption` | body | `string` | no | Optional video caption. |
| `chatId` | body | `string` | yes | Recipient chat ID. |
| `file` | body | `string` | yes | Public URL to the video. |
| `session` | body | `string` | yes | Session name from /api/sessions. |
