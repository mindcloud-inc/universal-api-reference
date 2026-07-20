# Extract Audio From Video with Eranol

Creates an audio extraction job in Eranol.

## Endpoint

- **Method:** `POST`
- **Path:** `/ffmpeg/video/extract/audio`
- **Base URL:** `https://eranol.com/api/v1`
- **Official documentation:** [Extract Audio From Video](https://www.eranol.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Source video URL |
| `mono` | body | `boolean` | no | Extract mono audio when true |
