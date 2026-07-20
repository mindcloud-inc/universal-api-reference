# Update Transcription Vocabulary with Mux

## Endpoint

- **Method:** `PUT`
- **Path:** `/video/v1/transcription-vocabularies/{TRANSCRIPTION_VOCABULARY_ID}`
- **Base URL:** `https://api.mux.com`
- **Official documentation:** [Update Transcription Vocabulary](https://www.mux.com/docs/api-reference/video/transcription-vocabularies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phrases[]` | body | `array<string>` | yes | The phrase list for the vocabulary. |
| `TRANSCRIPTION_VOCABULARY_ID` | path | `string` | yes | The transcription vocabulary ID. |
