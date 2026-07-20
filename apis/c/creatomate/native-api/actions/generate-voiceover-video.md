# Generate Voiceover Video with Creatomate

Creates a voiceover video render in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Generate Voiceover Video](https://creatomate.com/docs/api/quick-start/generate-a-voice-over-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `voiceoverText` | body | `string` | yes | Text to synthesize into the voiceover audio. |
| `voiceProvider` | body | `string` | no | Creatomate provider string for the speech engine and voice selection. |
