# Voice Dubbing with Runway

Creates a voice dubbing task in Runway.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/voice_dubbing`
- **Base URL:** `https://api.dev.runwayml.com`
- **Official documentation:** [Voice Dubbing](https://docs.dev.runwayml.com/api#tag/Start-generating/paths/~1v1~1voice_dubbing/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audioUri` | body | `string` | yes | HTTPS URL, Runway URI, or data URI for the source audio. |
| `disableVoiceCloning` | body | `boolean` | no | Whether to disable voice cloning and use a generic dubbed voice. |
| `dropBackgroundAudio` | body | `boolean` | no | Whether to remove background audio from the dubbed output. |
| `model` | body | `string` | yes | Runway currently requires eleven_voice_dubbing. |
| `numSpeakers` | body | `number` | no | Optional number of detected speakers in the source audio. |
| `targetLang` | body | `string` | yes | Target dubbing language code, such as es, fr, or de. |
