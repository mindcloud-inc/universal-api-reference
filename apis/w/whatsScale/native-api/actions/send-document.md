# Send Document with WhatsScale

Creates a document send job in WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/sendDocument`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Send Document](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caption` | body | `string` | no | Optional document caption. |
| `chatId` | body | `string` | yes | Recipient chat ID. |
| `file` | body | `string` | yes | Public URL to the document. |
| `filename` | body | `string` | no | Optional display filename for the document. |
| `session` | body | `string` | yes | Session name from /api/sessions. |
