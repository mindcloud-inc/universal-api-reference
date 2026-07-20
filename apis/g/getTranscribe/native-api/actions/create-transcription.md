# Create Transcription with GetTranscribe

Creates a transcription in GetTranscribe from a video URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/transcriptions`
- **Base URL:** `https://api.gettranscribe.ai`
- **Official documentation:** [Create Transcription](https://www.gettranscribe.ai/api-documentation/transcriptions/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The video URL to transcribe. |
| `folder_id` | body | `number` | no | Optional folder ID for organization. |
| `language` | body | `string` | no | Optional ISO-639-1 language code. |
| `model` | body | `string` | no | Optional transcription profile. Accepted values: `0`, `1`, `2`, `3`. |
| `prompt` | body | `string` | no | Optional context text to guide transcription. |
