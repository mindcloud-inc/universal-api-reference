# Convert Speech to Speech with Voicemaker

Creates converted speech from uploaded audio in Voicemaker.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/speech-to-speech`
- **Base URL:** `https://developer.voicemaker.in`
- **Official documentation:** [Convert Speech to Speech](https://developer.voicemaker.in/apidocs/speech-to-speech-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Source audio file to re-voice. |
| `VoiceId` | body | `string` | yes | Target ProPlus or cloned voice ID. |
| `OutputFormat` | body | `string` | no | Audio output format. |
| `SampleRate` | body | `number` | no | Output sample rate. |
| `ResponseType` | body | `string` | no | Response mode for generated audio. |
| `MasterVolume` | body | `number` | no | Volume adjustment from -20 to 20. |
| `MasterSpeed` | body | `number` | no | Speed adjustment from -100 to 100. |
| `MasterPitch` | body | `number` | no | Pitch adjustment from -100 to 100. |
