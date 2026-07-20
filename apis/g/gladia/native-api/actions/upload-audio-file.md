# Upload Audio File with Gladia

Uploads an audio file to Gladia.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/upload`
- **Base URL:** `https://api.gladia.io`
- **Official documentation:** [Upload Audio File](https://docs.gladia.io/api-reference/v2/upload/audio-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audio_url` | body | `string` | yes | External audio or video URL for Gladia to upload. |
