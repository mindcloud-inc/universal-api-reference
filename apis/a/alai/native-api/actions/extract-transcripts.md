# Extract Transcripts with Alai

Creates an async transcript extraction for an Alai presentation.

## Endpoint

- **Method:** `POST`
- **Path:** `/presentations/:presentation_id/transcripts`
- **Base URL:** `https://slides-api.getalai.com/api/v1`
- **Official documentation:** [Extract Transcripts](https://docs.getalai.com/api/generate-transcripts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentation_id` | path | `string` | yes | Presentation identifier to transcribe. |
