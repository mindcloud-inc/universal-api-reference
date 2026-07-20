# Create Transcription Job with Speech is Cheap

Creates a new transcription job in Speech is Cheap.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs/`
- **Base URL:** `https://api.speechischeap.com/v2`
- **Official documentation:** [Create Transcription Job](https://docs.speechischeap.com/jobs-v2/create/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input_url` | body | `string` | yes | Publicly accessible audio or video file URL to transcribe. |
| `webhook_url` | body | `string` | no | Optional URL where Speech is Cheap may POST transcription results. |
| `language` | body | `string` | no | Optional two-letter ISO 639-1 language code, such as en or es. Omit for auto-detection. |
| `can_label_audio` | body | `boolean` | no | When enabled, includes audio classification labels in transcription output. |
| `can_parse_speakers` | body | `boolean` | no | When enabled, includes speaker_id on each segment. |
| `can_parse_words` | body | `boolean` | no | When enabled, includes timestamps for each word. |
| `is_private` | body | `boolean` | no | When enabled, redacts the original input_url and deletes segments after 12 hours. |
| `minimum_confidence` | body | `number` | no | Filters out segments below this confidence threshold. Defaults to 0.5. |
| `segment_duration` | body | `number` | no | Transcription segment duration in seconds. Must be between 6 and 30. |
