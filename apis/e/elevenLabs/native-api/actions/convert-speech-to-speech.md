# Convert Speech To Speech with ElevenLabs

Transforms audio from one voice to another in ElevenLabs.

## Endpoint

- **Method:** `POST`
- **Path:** `/speech-to-speech/:voice_id`
- **Base URL:** `https://api.elevenlabs.io/v1`
- **Official documentation:** [Convert Speech To Speech](https://elevenlabs.io/docs/api-reference/speech-to-speech/convert)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voice_id` | path | `string` | yes | ID of the target voice. |
| `audio` | body | `file` | yes | Audio file or public file URL to convert. |
| `model_id` | body | `string` | no | Speech-to-speech model to use. |
| `voice_settings` | body | `string` | no | JSON-encoded voice settings override string. |
| `seed` | body | `number` | no | Deterministic sampling seed. |
| `remove_background_noise` | body | `boolean` | no | Whether to remove background noise before conversion. |
| `file_format` | body | `string` | no | Input audio format. |
| `output_format` | query | `string` | no | Generated audio output format. |
| `enable_logging` | query | `boolean` | no | Whether to retain history and request stitching. |
