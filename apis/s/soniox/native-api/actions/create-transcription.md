# Create transcription with Soniox

Creates a new transcription in Soniox.

## Endpoint

- **Method:** `POST`
- **Path:** `/transcriptions`
- **Base URL:** `https://api.soniox.com/v1`
- **Official documentation:** [Create transcription](https://soniox.com/docs/stt/api-reference/transcriptions/create_transcription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | Speech-to-text model to use for the transcription. |
| `audio_url` | body | `string` | no | Public URL of the audio file to transcribe. |
| `file_id` | body | `string` | no | Uploaded file ID to transcribe instead of an audio URL. |
| `language_hints[]` | body | `array<string>` | no | Expected languages in the audio. |
| `language_hints_strict` | body | `boolean` | no | Rely more heavily on the provided language hints. |
| `enable_speaker_diarization` | body | `boolean` | no | Identify and separate speakers in the transcription output. |
| `enable_language_identification` | body | `boolean` | no | Detect the language for each part of the transcription. |
| `translation.type` | body | `string` | no | Translation mode for the transcription. |
| `translation.target_language` | body | `string` | no | Target language for one-way translation. |
| `translation.language_a` | body | `string` | no | First language for two-way translation. |
| `translation.language_b` | body | `string` | no | Second language for two-way translation. |
| `context` | body | `string` | no | Additional context to improve transcription accuracy. |
| `webhook_url` | body | `string` | no | Webhook URL for completion or failure notifications. |
| `webhook_auth_header_name` | body | `string` | no | Name of the auth header sent with webhook notifications. |
| `webhook_auth_header_value` | body | `string` | no | Value of the auth header sent with webhook notifications. |
| `client_reference_id` | body | `string` | no | Optional tracking identifier for your system. |
