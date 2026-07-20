# Add Intro with Eranol

Creates an intro addition job in Eranol.

## Endpoint

- **Method:** `POST`
- **Path:** `/ffmpeg/video/add-intro`
- **Base URL:** `https://eranol.com/api/v1`
- **Official documentation:** [Add Intro](https://www.eranol.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `intro_url` | body | `string` | yes | Intro clip URL to prepend. |
| `url` | body | `string` | yes | Main video file URL. |
