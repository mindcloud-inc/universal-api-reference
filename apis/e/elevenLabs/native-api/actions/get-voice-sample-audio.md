# Get Voice Sample Audio with ElevenLabs

Retrieves voice sample audio from ElevenLabs.

## Endpoint

- **Method:** `GET`
- **Path:** `/voices/:voice_id/samples/:sample_id/audio`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [Get Voice Sample Audio](https://elevenlabs.io/docs/api-reference/voices/samples/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_id` | path | `string` | yes | The voice identifier. |
| `sample_id` | path | `string` | yes | The sample identifier. |
