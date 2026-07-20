# Post Text Story with WhatsScale

Creates a text story job in WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/status/text`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Post Text Story](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `backgroundColor` | body | `string` | no | Optional hex background color for the text story. |
| `font` | body | `number` | no | Optional WhatsApp story font style number. |
| `session` | body | `string` | yes | Session name from /api/sessions. |
| `text` | body | `string` | yes | Status text. |
