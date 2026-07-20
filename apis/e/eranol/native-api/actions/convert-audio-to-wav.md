# Convert Audio To WAV with Eranol

Creates a WAV conversion job in Eranol.

## Endpoint

- **Method:** `POST`
- **Path:** `/ffmpeg/convert/audio/to/wav`
- **Base URL:** `https://eranol.com/api/v1`
- **Official documentation:** [Convert Audio To WAV](https://www.eranol.com/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Audio file URL to convert to WAV. |
