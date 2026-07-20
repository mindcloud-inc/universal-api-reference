# Post Image Story with WhatsScale

Creates an image story job in WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/status/image`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Post Image Story](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caption` | body | `string` | no | Optional image story caption. |
| `file` | body | `string` | yes | Public URL to the image. |
| `session` | body | `string` | yes | Session name from /api/sessions. |
