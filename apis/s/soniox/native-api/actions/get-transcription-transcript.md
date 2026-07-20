# Get transcription transcript with Soniox

Retrieves transcript text for a Soniox transcription.

## Endpoint

- **Method:** `GET`
- **Path:** `/transcriptions/:transcription_id/transcript`
- **Base URL:** `https://api.soniox.com/v1`
- **Official documentation:** [Get transcription transcript](https://soniox.com/docs/stt/api-reference/transcriptions/get_transcription_transcript)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcription_id` | path | `string` | yes | Unique identifier of the transcription. |
