# Generate TTS with Voicemaker

Creates synthesized speech from text in Voicemaker.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/voice/convert`
- **Base URL:** `https://developer.voicemaker.in`
- **Official documentation:** [Generate TTS](https://developer.voicemaker.in/apidocs/generate-tts)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `VoiceId` | body | `string` | yes | Voice ID to synthesize with, for example ai3-Jony. |
| `LanguageCode` | body | `string` | yes | Language code for the selected voice, for example en-US. |
| `Text` | body | `string` | yes | Text or SSML content to convert to speech. |
| `OutputFormat` | body | `string` | no | Audio format such as mp3, wav, ogg, opus, aac, ulaw, or alaw. |
| `SampleRate` | body | `number` | no | Sample rate, for example 22050, 24000, 44100, or 48000. |
| `MasterVolume` | body | `number` | no | Volume adjustment from -20 to 20. |
| `MasterSpeed` | body | `number` | no | Speed adjustment from -100 to 100. |
| `MasterPitch` | body | `number` | no | Pitch adjustment from -100 to 100. |
