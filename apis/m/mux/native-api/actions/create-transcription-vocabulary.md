# Create Transcription Vocabulary with Mux

## Endpoint

- **Method:** `POST`
- **Path:** `/video/v1/transcription-vocabularies`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Create Transcription Vocabulary](https://www.mux.com/docs/api-reference/video/transcription-vocabularies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phrases[]` | body | `array<string>` | yes | The phrase list for the vocabulary. |
