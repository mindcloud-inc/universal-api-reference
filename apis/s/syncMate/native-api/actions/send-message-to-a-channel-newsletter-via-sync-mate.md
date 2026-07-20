# Send Message To A Channel/Newsletter Via SyncMate with SyncMate

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/wapushplus/single/message`
- **Base URL:** `https://app.assistro.co`
- **Official documentation:** [Send Message To A Channel/Newsletter Via SyncMate](https://assistro.co/user-guide/zapier/how-to-send-a-whatsapp-notification-to-any-group-or-channel/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msgs[]` | body | `array<object>` | yes | — |
| `msgs[].number` | body | `string` | yes | WhatsApp channel or newsletter ID ending in @newsletter. |
| `msgs[].message` | body | `string` | yes | — |
| `msgs[].media[]` | body | `array<object>` | no | — |
| `msgs[].media[].media_base64` | body | `string` | no | Raw base64 string without the MIME type prefix. |
| `msgs[].media[].file_name` | body | `string` | no | — |
