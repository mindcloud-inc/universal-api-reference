# Generate TTS with VoxFX with Voicemaker

Creates synthesized speech with VoxFX in Voicemaker.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/voice/convert`
- **Base URL:** `https://developer.voicemaker.in`
- **Official documentation:** [Generate TTS with VoxFX](https://developer.voicemaker.in/apidocs/generate-tts-with-voxfx)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `VoiceId` | body | `string` | yes | Voice ID to synthesize with. |
| `LanguageCode` | body | `string` | yes | Language code for the selected voice. |
| `Text` | body | `string` | yes | Text or SSML content to convert to speech. |
| `OutputFormat` | body | `string` | no | Audio format such as mp3 or wav. |
| `VoxFx` | body | `object` | yes | VoxFX configuration object including presetId and optional effects overrides. |
