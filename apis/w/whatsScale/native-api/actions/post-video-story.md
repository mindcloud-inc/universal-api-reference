# Post Video Story with WhatsScale

Creates a video story job in WhatsScale.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/status/video`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Post Video Story](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `caption` | body | `string` | no | Optional video story caption. |
| `file` | body | `string` | yes | Public URL to the video. |
| `session` | body | `string` | yes | Session name from /api/sessions. |
