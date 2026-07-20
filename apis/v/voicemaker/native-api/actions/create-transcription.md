# Create Transcription with Voicemaker

Creates a transcription from audio in Voicemaker.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/speech-to-text`
- **Base URL:** `https://developer.voicemaker.in`
- **Official documentation:** [Create Transcription](https://developer.voicemaker.in/apidocs/speech-to-text-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Audio file to transcribe. |
| `model` | body | `string` | no | Transcription model, for example stt-flagship-v1. |
| `language` | body | `string` | no | Language code or auto for auto-detection. |
| `responseFormat` | body | `string` | no | Desired transcription response format. |
| `includeSubtitle` | body | `boolean` | no | Whether to include subtitle output. |
| `tagAudioEvents` | body | `boolean` | no | Whether to tag audio events in the transcription. |
