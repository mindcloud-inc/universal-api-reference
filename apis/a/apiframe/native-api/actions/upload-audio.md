# Upload Audio with Apiframe

Uploads audio to Apiframe and returns a song task ID and URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/suno-upload`
- **Base URL:** `https://api.apiframe.pro`
- **Official documentation:** [Upload Audio](https://docs.apiframe.ai/suno-ai-api/upload)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `audio` | body | `file` | yes |
