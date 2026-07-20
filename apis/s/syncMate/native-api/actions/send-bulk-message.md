# Send Bulk Message with SyncMate

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/wapushplus/bulk/message`
- **Base URL:** `https://app.assistro.co`
- **Official documentation:** [Send Bulk Message](https://assistro.co/user-guide/developer-guide/connect-your-custom-app-with-syncmate/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msgs[]` | body | `array<object>` | yes | — |
| `msgs[].number` | body | `string` | yes | WhatsApp number with country code and no plus sign. |
| `msgs[].message` | body | `string` | yes | — |
| `msgs[].media[]` | body | `array<object>` | no | — |
| `msgs[].media[].media_base64` | body | `string` | no | Raw base64 string without the MIME type prefix. |
| `msgs[].media[].file_name` | body | `string` | no | — |
